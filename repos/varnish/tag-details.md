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
$ docker pull varnish@sha256:fae44b93f72c103a1b07ef5046d3969ef43d6abed9d0637c6defee605d6c1aa5
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
$ docker pull varnish@sha256:5360318539dc8b05fed21a56d06012897d8af9c24b26bcafb0b5308afbf1fb9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95861714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5385e986c1d5875ef038b503478bf76b2fc9f20f7cdbe33f1903c9305f4e926`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:58:49 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:58:49 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:58:49 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:58:49 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:00:41 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 05:00:42 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:00:42 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:00:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:00:42 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:00:42 GMT
CMD []
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4769cf1c2ed5001dd80925ff94b3ec6e9ec0590f9616de69fee984cb032b958`  
		Last Modified: Tue, 02 Jul 2024 05:09:32 GMT  
		Size: 64.4 MB (64438714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fc65480a218650c313c4a173739cc2cc2e0d6c6afe08e9f19d3dee30174724`  
		Last Modified: Tue, 02 Jul 2024 05:09:23 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:486b9ce4259d2561cbb8351e9399b0e7a37d46a5b54686ee171db952b6340a95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72858021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0068cb3ef05f75aff684597cef85b1ec67250cdbc036a34a3334eaf33d4edaf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:18:37 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:18:37 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:18:37 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:18:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:20:17 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:20:17 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:20:18 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:20:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:20:18 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:20:18 GMT
CMD []
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13aaf79ba297cbd68c00cf789f9ea5b12a54286f7866d0da0b9a2a59da5562`  
		Last Modified: Tue, 02 Jul 2024 04:28:54 GMT  
		Size: 46.3 MB (46274599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5d92f8b4f09f971eaade8d1c87937f7806fdb4e56674d1128ac335d6b702be`  
		Last Modified: Tue, 02 Jul 2024 04:28:48 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:bd45ac8e31ba63a70c63cf2a4265796b8d305d8404e98cdbe6b2ed1a599fa165
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89958871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad02409b9bf71292b1cea6c39522bb99d628f3f3599e9297809586c6f1bc2ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:17:10 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:17:10 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:17:10 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:17:10 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:18:37 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:18:38 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:18:38 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:18:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:18:38 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:18:38 GMT
CMD []
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153d5c1d94c4804c2f448d050f817e1b3a110b3691de7cfb3783dff8879b6071`  
		Last Modified: Tue, 02 Jul 2024 04:26:05 GMT  
		Size: 59.9 MB (59888542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9376107d7d3e15b00fa56b3254347d2a47b17033daf68faa87e04a8ffb4df72b`  
		Last Modified: Tue, 02 Jul 2024 04:25:58 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:f1dc85300798a3e31f0c1b60936cd276cd10fe553296882d451213d5fc6399d8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97129607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f53ffb2d85e94505ed523fa67cc60f4ed3a62eec09e4526fa7167d51650a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:18 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 01:26:19 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 01:26:19 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 01:26:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:28:31 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 01:28:32 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:28:32 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:28:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:28:32 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:28:33 GMT
CMD []
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa8474d680a30423f88095d021431e2a707a59c23532c6c3c33bfc2e6a407c`  
		Last Modified: Tue, 02 Jul 2024 01:38:53 GMT  
		Size: 64.7 MB (64720438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b6d78caf142afa6cbc9dbed69d2647deb8f6f6dd544fda612138aef734af0`  
		Last Modified: Tue, 02 Jul 2024 01:38:41 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:c74197383e5c1f4b20ae2339761ca885a98b272697c13be553456aaf81dadad7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94652569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91f64258a18157b0d658c98a06d27accdaf80f15e638c7793992363cdcaade8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:07:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 23 Jul 2024 02:07:54 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 23 Jul 2024 02:07:54 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 23 Jul 2024 02:07:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:11:09 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 02:11:12 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:11:12 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:11:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:11:13 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:11:14 GMT
CMD []
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22da0b5a4215694a5c74a41f0204a084ef5fbbbfcf338b0415ac36afe9623b0d`  
		Last Modified: Tue, 23 Jul 2024 02:24:24 GMT  
		Size: 59.3 MB (59346651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93a758e1759711d142c2eb2130e6323ef163a6c103b397fdccd3da8c01b16d`  
		Last Modified: Tue, 23 Jul 2024 02:24:14 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:94b3253a58f856134ae2d7d5aae089fdf6bc02565013c66ea9939499ed87a6d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fad799339b5dd8c54c2033c029e361a51f86ed2b63c01777d15ddab2fff735e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:21:39 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 03:21:39 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 03:21:39 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 03:21:39 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:23:30 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 03:23:31 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:23:31 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:23:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:23:31 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:23:32 GMT
CMD []
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5719f582c9346191e5e2cc39cb6fd6647b2ff915cbcd2c11d34b6ddb7d43d019`  
		Last Modified: Tue, 02 Jul 2024 03:31:36 GMT  
		Size: 46.6 MB (46595231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c364ebc518cea7f92cc62c044945fa809d7deb10db3e7c59fdd793a80d20d73d`  
		Last Modified: Tue, 02 Jul 2024 03:31:29 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.12`

```console
$ docker pull varnish@sha256:dc2bdf906ca8a18a1fb90f6304c729153974e76b7f2950c93f330e10ee28a77d
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
$ docker pull varnish@sha256:302e5f4cbe467171b3a33d7a08b025962e00e63277c1efb4d986346bdefc84c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95856270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ddd93807eff65d6aef8b70f59f56706366040b712d346edf0feda9da4f807a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:06:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:08:03 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 05:08:04 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:08:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:08:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:08:04 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:08:05 GMT
CMD []
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e488c5cbd63f44b88c4f4d4709a24bbb4301957c7169c33bee8bfdc7f39e59f2`  
		Last Modified: Tue, 02 Jul 2024 05:10:28 GMT  
		Size: 64.4 MB (64433288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949239f035d7490fab1ce1622e132325020b655e2eec9c944a3b0d31eb8d5c3b`  
		Last Modified: Tue, 02 Jul 2024 05:10:20 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; arm variant v7

```console
$ docker pull varnish@sha256:ab4b2f9c1228e06a9df725452d4d87aab3c741287d78eea21f41d09c60029663
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72855682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948c59955f4817e31c94a9f6ee1220803eb5143da7ab541bef6f2a369f4be920`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:25:49 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:27:29 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:27:29 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:27:29 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:27:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:27:29 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:27:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a508fc68f9005f5017ccbfc2733c0848da7da31ae4ee95cfaacd1c6dcd9baa3`  
		Last Modified: Tue, 02 Jul 2024 04:29:43 GMT  
		Size: 46.3 MB (46272276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12592c39082f9a37aff727a6b93b82b7d19af8f7cdd75d806fcedcd0617f1948`  
		Last Modified: Tue, 02 Jul 2024 04:29:37 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:92527f1ada148519209ca131ebe03ecee8de383b6a92bbdc03d801d208862630
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89953577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878c020e9cfd24d96379cdd3732fb347f094d390949d4f4fe687c3394174024d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:23:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:24:47 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:24:48 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:24:48 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:24:48 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:24:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a40a65e792c6772928d0dff0ddab0e588cb67f88952e6b3f0604b35f888136c`  
		Last Modified: Tue, 02 Jul 2024 04:26:52 GMT  
		Size: 59.9 MB (59883262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34f6a2b6f1324165fb1c99a8e8094604aa34c86c0368775c773b4f44f75303d`  
		Last Modified: Tue, 02 Jul 2024 04:26:46 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; 386

```console
$ docker pull varnish@sha256:66294f4774cb820d2ffb3736a84503accfe3d807b3517ece8af8a020571ce01d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97124339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edee7ff0668d0fc4c049686eff48974de0e3125dfb819f4a6aa550512f34ccec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:35:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:37:16 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 01:37:16 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:37:17 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:37:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:37:17 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:37:17 GMT
CMD []
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c7f19f079b954528facdf94b4f9e31f6b630349690cd33f946ad00e99a7cb`  
		Last Modified: Tue, 02 Jul 2024 01:40:02 GMT  
		Size: 64.7 MB (64715187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be073aa2bf46a8af81b6c85e38b1b0084edbd86e37370261f13ffd9765fa0e6`  
		Last Modified: Tue, 02 Jul 2024 01:39:51 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; ppc64le

```console
$ docker pull varnish@sha256:ae12dffc8cb995f039080e7a5dbc79c8126b0b04dc8db67b402dc56932153f83
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94647321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad0dca065e9f2cd6a7ac2b355f9e4d0313a942b6f696f4dd1586c08bd648858`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:19:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:22:56 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 02:22:58 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:22:58 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:22:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:22:59 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:22:59 GMT
CMD []
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb4536f4ac3e2f093f7dfa34dd28318844e13868dc9d4a5632107baaec59677`  
		Last Modified: Tue, 23 Jul 2024 02:25:24 GMT  
		Size: 59.3 MB (59341417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1f5c75d3822911e9350b1db0afc3cd48095a29f745fb138edaf25da9c6ba96`  
		Last Modified: Tue, 23 Jul 2024 02:25:14 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; s390x

```console
$ docker pull varnish@sha256:5aff2d24f4ee254f5cd04f7e29b529af58b74601d3f3c40455bc3a9f973ecc4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76253806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890879ee818e59e82f4fa8cf366902a4d4854da8fa1922cea0d5d9a0c14be5e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:29:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:30:23 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 03:30:25 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:30:25 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:30:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:30:25 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:30:26 GMT
CMD []
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7f824b699f0e36f63bc2c6edca2d9b17b85ba9dada599c6661392e4757c538`  
		Last Modified: Tue, 02 Jul 2024 03:32:18 GMT  
		Size: 46.6 MB (46590751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe9e33d65db26215c2f4b29098bbc4049c3c9a1d53ada55a02ff095c5d6178`  
		Last Modified: Tue, 02 Jul 2024 03:32:12 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:fae44b93f72c103a1b07ef5046d3969ef43d6abed9d0637c6defee605d6c1aa5
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
$ docker pull varnish@sha256:5360318539dc8b05fed21a56d06012897d8af9c24b26bcafb0b5308afbf1fb9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95861714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5385e986c1d5875ef038b503478bf76b2fc9f20f7cdbe33f1903c9305f4e926`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:58:49 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:58:49 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:58:49 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:58:49 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:00:41 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 05:00:42 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:00:42 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:00:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:00:42 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:00:42 GMT
CMD []
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4769cf1c2ed5001dd80925ff94b3ec6e9ec0590f9616de69fee984cb032b958`  
		Last Modified: Tue, 02 Jul 2024 05:09:32 GMT  
		Size: 64.4 MB (64438714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fc65480a218650c313c4a173739cc2cc2e0d6c6afe08e9f19d3dee30174724`  
		Last Modified: Tue, 02 Jul 2024 05:09:23 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:486b9ce4259d2561cbb8351e9399b0e7a37d46a5b54686ee171db952b6340a95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72858021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0068cb3ef05f75aff684597cef85b1ec67250cdbc036a34a3334eaf33d4edaf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:18:37 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:18:37 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:18:37 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:18:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:20:17 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:20:17 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:20:18 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:20:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:20:18 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:20:18 GMT
CMD []
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13aaf79ba297cbd68c00cf789f9ea5b12a54286f7866d0da0b9a2a59da5562`  
		Last Modified: Tue, 02 Jul 2024 04:28:54 GMT  
		Size: 46.3 MB (46274599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5d92f8b4f09f971eaade8d1c87937f7806fdb4e56674d1128ac335d6b702be`  
		Last Modified: Tue, 02 Jul 2024 04:28:48 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:bd45ac8e31ba63a70c63cf2a4265796b8d305d8404e98cdbe6b2ed1a599fa165
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89958871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad02409b9bf71292b1cea6c39522bb99d628f3f3599e9297809586c6f1bc2ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:17:10 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:17:10 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:17:10 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:17:10 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:18:37 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:18:38 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:18:38 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:18:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:18:38 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:18:38 GMT
CMD []
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153d5c1d94c4804c2f448d050f817e1b3a110b3691de7cfb3783dff8879b6071`  
		Last Modified: Tue, 02 Jul 2024 04:26:05 GMT  
		Size: 59.9 MB (59888542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9376107d7d3e15b00fa56b3254347d2a47b17033daf68faa87e04a8ffb4df72b`  
		Last Modified: Tue, 02 Jul 2024 04:25:58 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:f1dc85300798a3e31f0c1b60936cd276cd10fe553296882d451213d5fc6399d8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97129607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f53ffb2d85e94505ed523fa67cc60f4ed3a62eec09e4526fa7167d51650a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:18 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 01:26:19 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 01:26:19 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 01:26:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:28:31 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 01:28:32 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:28:32 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:28:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:28:32 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:28:33 GMT
CMD []
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa8474d680a30423f88095d021431e2a707a59c23532c6c3c33bfc2e6a407c`  
		Last Modified: Tue, 02 Jul 2024 01:38:53 GMT  
		Size: 64.7 MB (64720438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b6d78caf142afa6cbc9dbed69d2647deb8f6f6dd544fda612138aef734af0`  
		Last Modified: Tue, 02 Jul 2024 01:38:41 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:c74197383e5c1f4b20ae2339761ca885a98b272697c13be553456aaf81dadad7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94652569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91f64258a18157b0d658c98a06d27accdaf80f15e638c7793992363cdcaade8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:07:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 23 Jul 2024 02:07:54 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 23 Jul 2024 02:07:54 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 23 Jul 2024 02:07:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:11:09 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 02:11:12 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:11:12 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:11:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:11:13 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:11:14 GMT
CMD []
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22da0b5a4215694a5c74a41f0204a084ef5fbbbfcf338b0415ac36afe9623b0d`  
		Last Modified: Tue, 23 Jul 2024 02:24:24 GMT  
		Size: 59.3 MB (59346651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93a758e1759711d142c2eb2130e6323ef163a6c103b397fdccd3da8c01b16d`  
		Last Modified: Tue, 23 Jul 2024 02:24:14 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:94b3253a58f856134ae2d7d5aae089fdf6bc02565013c66ea9939499ed87a6d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fad799339b5dd8c54c2033c029e361a51f86ed2b63c01777d15ddab2fff735e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:21:39 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 03:21:39 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 03:21:39 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 03:21:39 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:23:30 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 03:23:31 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:23:31 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:23:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:23:31 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:23:32 GMT
CMD []
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5719f582c9346191e5e2cc39cb6fd6647b2ff915cbcd2c11d34b6ddb7d43d019`  
		Last Modified: Tue, 02 Jul 2024 03:31:36 GMT  
		Size: 46.6 MB (46595231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c364ebc518cea7f92cc62c044945fa809d7deb10db3e7c59fdd793a80d20d73d`  
		Last Modified: Tue, 02 Jul 2024 03:31:29 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3`

```console
$ docker pull varnish@sha256:7a849efdd9b60947db625613049f2f1fd9c012090e854942d3c2670dfcef6e71
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
$ docker pull varnish@sha256:3ce3afb27a5b1f78af38de49bb1bd6ca9d050c21a74925eccabb964acd41fbff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101971591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b526d36083c554794205c57662e2f3c823220250b445a5d05be35d03818bcb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:03:39 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 05:03:39 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 05:03:39 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 05:03:40 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 05:03:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 05:03:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:06:06 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 05:06:07 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:06:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:06:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:06:07 GMT
USER varnish
# Tue, 02 Jul 2024 05:06:07 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:06:07 GMT
CMD []
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fe3ad246d1e4aea38b6f20890df8e4e623119ebdb8654e808b4555298b1a0`  
		Last Modified: Tue, 02 Jul 2024 05:10:11 GMT  
		Size: 70.5 MB (70548815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77f783e64cc308d9b9977bae1935ea9fa53d7360a795e5dde16868e5ee63505`  
		Last Modified: Tue, 02 Jul 2024 05:10:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:976b1b1cb191710c5fe62fc7d9edf05faa4825318d5fb684cf8a6be982b28c46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78760457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd220ab2d90d35ef695ae717782166a695ec5b75c8e49100f81ef35e47e0fc0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:23:10 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 04:23:10 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 04:23:11 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 04:23:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:23:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:25:30 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 04:25:31 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:25:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:25:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:25:31 GMT
USER varnish
# Tue, 02 Jul 2024 04:25:31 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:25:32 GMT
CMD []
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147f29f56cd08544d3e57cf625650f8936720e211e20c1aef86721c65d27ed3f`  
		Last Modified: Tue, 02 Jul 2024 04:29:28 GMT  
		Size: 52.2 MB (52177261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24a36b13be19daafcbec4f0efb37e98f6b5b7df533bca82e4aa0eff4efcf306`  
		Last Modified: Tue, 02 Jul 2024 04:29:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e4f845c0b04545c09da07fa072127da918a09316f8b07164ae6757b867ed892b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95792827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795164c05a0c3164e53ecbb18765840f28aa68469c6bbb5b785c5bce075dc220`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:21:13 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 04:21:13 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 04:21:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 04:21:14 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 04:21:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:21:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:23:18 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 04:23:18 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:23:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:23:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:23:19 GMT
USER varnish
# Tue, 02 Jul 2024 04:23:19 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:23:19 GMT
CMD []
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2991aa82325f3b198fc390a7e4b780f14b7e42a169dc4c9c65f48e71d1ef15b2`  
		Last Modified: Tue, 02 Jul 2024 04:26:37 GMT  
		Size: 65.7 MB (65722721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6900ae6b39def6c771779a8f7475d1727174362ba1600f0c2ddeeaeb7821a2f`  
		Last Modified: Tue, 02 Jul 2024 04:26:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; 386

```console
$ docker pull varnish@sha256:0428b5fbc86c3cd994e766ea74b781740a1d28d1dd93ce83ebed1a511f5e5cd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103220035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6983b069961004bcfffc3dd8ae526718046d92d969f6bf8ac004946f957a709d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:32:06 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 01:32:06 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 01:32:07 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 01:32:07 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 01:32:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:32:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:35:06 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 01:35:07 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:35:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:35:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:35:07 GMT
USER varnish
# Tue, 02 Jul 2024 01:35:07 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:35:07 GMT
CMD []
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d8025bdfa81a47a5ef5264f6345956388076a9540bdd63049e8717c65f6266`  
		Last Modified: Tue, 02 Jul 2024 01:39:42 GMT  
		Size: 70.8 MB (70811091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a294f3f5dfd677171a5e33f20528eacdd28a45fdb7ecca5c0aeb3345a6d489`  
		Last Modified: Tue, 02 Jul 2024 01:39:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:afcf9c6e22d9488cf7b9a2fdfb443c9b8b77229e5544133304dbf709d5bf7f13
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100899050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f0a47849f2dd61524955cf1971d1d9d1546c280402a997d22babd9750b3ce8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:15:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 02:15:46 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 02:15:47 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 02:15:48 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:15:48 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:15:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 02:15:49 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 02:15:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 02:15:50 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:15:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 02:15:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:19:33 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:19:35 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:19:36 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:19:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:19:36 GMT
USER varnish
# Tue, 23 Jul 2024 02:19:37 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:19:38 GMT
CMD []
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261aa3d6f91e5767731a54a44a79d81d51b826a9d3a8fbac7b5c43cadeb68f52`  
		Last Modified: Tue, 23 Jul 2024 02:25:06 GMT  
		Size: 65.6 MB (65593356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ea5dee4ebd467dc96328bee533836edc95457a05eb91361cf28341a9ecaa50`  
		Last Modified: Tue, 23 Jul 2024 02:24:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; s390x

```console
$ docker pull varnish@sha256:fd48e360aacb5e383ae21bde72ca1a44ee798e12131d09c33dfd520c73448fc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82344167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea6db8fb1fb3dacb1a627324488913688a52483f445ba12a7f9f7777009856`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:26:30 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 03:26:31 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 03:26:31 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 03:26:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:26:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:28:35 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 03:28:37 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:28:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:28:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:28:37 GMT
USER varnish
# Tue, 02 Jul 2024 03:28:37 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:28:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a97b7ea2be3a28ebe237bdb35d3cdd9927e9942174534b7ab93622470a80098`  
		Last Modified: Tue, 02 Jul 2024 03:32:06 GMT  
		Size: 52.7 MB (52681323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb29d185f36b2b415b543aca361fdf490f1b95b399e2851e846a51fc95bc87e`  
		Last Modified: Tue, 02 Jul 2024 03:31:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3-alpine`

```console
$ docker pull varnish@sha256:a379160a6dae442565f2c49eb98a15abc5de1eb8bd0809ada5227c2e48477d58
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
$ docker pull varnish@sha256:0adc1921d1d1720a0e2acb6a4e929995f941b9125740338ec9ab3f304321c96a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16607ac683a4c560af2b4b117b9141a26538ff670f13f4fc3a364525253b0f1b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:23:05 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 00:23:05 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 00:23:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 00:23:06 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 00:23:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:23:06 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:24:27 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 00:24:28 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:24:28 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:24:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:24:28 GMT
USER varnish
# Tue, 23 Jul 2024 00:24:28 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:24:28 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83326aa66c31fadc8458f81f1864bd04c8b4c60081de4a49b74922c676d635c9`  
		Last Modified: Tue, 23 Jul 2024 00:26:03 GMT  
		Size: 69.6 MB (69561252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd4e5390f3d7cb29efe85bdd5ede79a3d86d2b91d9ecc9d022cb71611732890`  
		Last Modified: Tue, 23 Jul 2024 00:25:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7324d024edaf8bd09443e2bfafb5d288c078cd624349d08d9f22be26ab1d7c82
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57175436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a3d615fde91caf8c56472ecad9793bb874dc968fb6bdd989c215dc21d6e0f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:31:07 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 01:31:07 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 01:31:07 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 01:31:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:31:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:31:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 01:31:08 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 01:31:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 01:31:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 01:31:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:31:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:32:47 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:32:48 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:32:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:32:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:32:49 GMT
USER varnish
# Tue, 23 Jul 2024 01:32:49 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:32:49 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f6babe1551ab9ea2b7cfc585c356c4edae5f09f5a1ccf5fa70285301eb80`  
		Last Modified: Tue, 23 Jul 2024 01:34:13 GMT  
		Size: 54.2 MB (54247835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47fb0a3f15390b7abe7011284acb4e7fd4f7a1fa4398d9637269502dc2d70e1`  
		Last Modified: Tue, 23 Jul 2024 01:34:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:62789f930de4b24b5a49321c8ebdc3d6dfd0736719fadf1758b0342649e47871
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69688585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f934a0bd73c2f559fd959036b280a0ae21eae9bfbbec5c49a1ced6b90aea4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:40:04 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 02:40:04 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 02:40:05 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:40:05 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:40:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:41:14 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:41:14 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:41:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:41:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:41:14 GMT
USER varnish
# Tue, 23 Jul 2024 02:41:14 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:41:14 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f7b7f792e9ab0691612c5cc4462b434b6a3430557c497e375f9e1df0b5b98`  
		Last Modified: Tue, 23 Jul 2024 02:42:34 GMT  
		Size: 66.3 MB (66329632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191b9d3aecee2d005b4c90e24d361a83822606192e1fefa21118026139a2244`  
		Last Modified: Tue, 23 Jul 2024 02:42:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:90e0591def8ee13145f21b5daa90c5ef6bbbdbdf75853b978fd6781315b5caca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75010016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e96aa01f1d1a0d2054c348a13f4171bdbddc68288b25a4a17279ffebe1cb02b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:34:07 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 02:34:07 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 02:34:07 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 02:34:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:34:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:34:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 02:34:08 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 02:34:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 02:34:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:34:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:34:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:36:05 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:36:06 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:36:06 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:36:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:36:06 GMT
USER varnish
# Tue, 23 Jul 2024 02:36:07 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:36:07 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dac172d995b3618699d65633ad737f356c1ee1615ed90d167fe55bc0ede7dc`  
		Last Modified: Tue, 23 Jul 2024 02:37:46 GMT  
		Size: 71.8 MB (71756918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c596726176897bfbc5e1187c5feb0dbcca7befe485f468f33f16900272a18c19`  
		Last Modified: Tue, 23 Jul 2024 02:37:33 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:830afd90dff1a8c9b4aa1352b9c85ece58fd053ce8dff14309e101affe558ad0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70493238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d98a12aca2c2a82d469aba2c55840b7e23d7b0c1c1feeb5954eefd5507bbe8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:58:13 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Mon, 22 Jul 2024 23:58:13 GMT
ARG VARNISH_VERSION=7.3.1
# Mon, 22 Jul 2024 23:58:14 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Mon, 22 Jul 2024 23:58:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Mon, 22 Jul 2024 23:58:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Mon, 22 Jul 2024 23:58:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Mon, 22 Jul 2024 23:58:15 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Mon, 22 Jul 2024 23:58:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Mon, 22 Jul 2024 23:58:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Mon, 22 Jul 2024 23:58:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:58:16 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:59:33 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Mon, 22 Jul 2024 23:59:35 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:59:36 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:59:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:59:36 GMT
USER varnish
# Mon, 22 Jul 2024 23:59:36 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:59:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2137ef36fe0bb86ba613c917d08339e19a324d7daa6eb3b6fb32870c8e504`  
		Last Modified: Tue, 23 Jul 2024 00:01:25 GMT  
		Size: 67.1 MB (67129638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a486144facf2ca024b10033d6e95cdc74facb2e458be54c098ed14ad0f336325`  
		Last Modified: Tue, 23 Jul 2024 00:01:15 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:31af442f5488b1f91a18328914449a93cf1451a716977d9cecc8f401c5a0f240
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64885502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b312cbd3c4bcb02ffa1af91db33e071fd3d6c2a4667ee0cf4a828b85b092c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:11:53 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 01:11:53 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 01:11:53 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 01:11:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:11:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:13:14 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:13:16 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:13:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:13:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:13:17 GMT
USER varnish
# Tue, 23 Jul 2024 01:13:17 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:13:17 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5647f1c4c5339269d6f8beb83d37eaede42d4814019c3763d4467d4ba4d2402`  
		Last Modified: Tue, 23 Jul 2024 01:14:43 GMT  
		Size: 61.6 MB (61631930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a040b2bc0129a07fb0b698b4897dc3fc4a9501f221926a878282037b5987b36`  
		Last Modified: Tue, 23 Jul 2024 01:14:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3.1`

```console
$ docker pull varnish@sha256:7a849efdd9b60947db625613049f2f1fd9c012090e854942d3c2670dfcef6e71
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
$ docker pull varnish@sha256:3ce3afb27a5b1f78af38de49bb1bd6ca9d050c21a74925eccabb964acd41fbff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101971591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b526d36083c554794205c57662e2f3c823220250b445a5d05be35d03818bcb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:03:39 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 05:03:39 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 05:03:39 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 05:03:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 05:03:40 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 05:03:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 05:03:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:06:06 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 05:06:07 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:06:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:06:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:06:07 GMT
USER varnish
# Tue, 02 Jul 2024 05:06:07 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:06:07 GMT
CMD []
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fe3ad246d1e4aea38b6f20890df8e4e623119ebdb8654e808b4555298b1a0`  
		Last Modified: Tue, 02 Jul 2024 05:10:11 GMT  
		Size: 70.5 MB (70548815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77f783e64cc308d9b9977bae1935ea9fa53d7360a795e5dde16868e5ee63505`  
		Last Modified: Tue, 02 Jul 2024 05:10:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:976b1b1cb191710c5fe62fc7d9edf05faa4825318d5fb684cf8a6be982b28c46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78760457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd220ab2d90d35ef695ae717782166a695ec5b75c8e49100f81ef35e47e0fc0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:23:10 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 04:23:10 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 04:23:10 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 04:23:11 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 04:23:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:23:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:25:30 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 04:25:31 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:25:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:25:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:25:31 GMT
USER varnish
# Tue, 02 Jul 2024 04:25:31 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:25:32 GMT
CMD []
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147f29f56cd08544d3e57cf625650f8936720e211e20c1aef86721c65d27ed3f`  
		Last Modified: Tue, 02 Jul 2024 04:29:28 GMT  
		Size: 52.2 MB (52177261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24a36b13be19daafcbec4f0efb37e98f6b5b7df533bca82e4aa0eff4efcf306`  
		Last Modified: Tue, 02 Jul 2024 04:29:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e4f845c0b04545c09da07fa072127da918a09316f8b07164ae6757b867ed892b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95792827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795164c05a0c3164e53ecbb18765840f28aa68469c6bbb5b785c5bce075dc220`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:21:13 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 04:21:13 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 04:21:13 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 04:21:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 04:21:14 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 04:21:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:21:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:23:18 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 04:23:18 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:23:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:23:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:23:19 GMT
USER varnish
# Tue, 02 Jul 2024 04:23:19 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:23:19 GMT
CMD []
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2991aa82325f3b198fc390a7e4b780f14b7e42a169dc4c9c65f48e71d1ef15b2`  
		Last Modified: Tue, 02 Jul 2024 04:26:37 GMT  
		Size: 65.7 MB (65722721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6900ae6b39def6c771779a8f7475d1727174362ba1600f0c2ddeeaeb7821a2f`  
		Last Modified: Tue, 02 Jul 2024 04:26:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; 386

```console
$ docker pull varnish@sha256:0428b5fbc86c3cd994e766ea74b781740a1d28d1dd93ce83ebed1a511f5e5cd7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103220035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6983b069961004bcfffc3dd8ae526718046d92d969f6bf8ac004946f957a709d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:32:06 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 01:32:06 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 01:32:07 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 01:32:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 01:32:07 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 01:32:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:32:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:35:06 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 01:35:07 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:35:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:35:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:35:07 GMT
USER varnish
# Tue, 02 Jul 2024 01:35:07 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:35:07 GMT
CMD []
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d8025bdfa81a47a5ef5264f6345956388076a9540bdd63049e8717c65f6266`  
		Last Modified: Tue, 02 Jul 2024 01:39:42 GMT  
		Size: 70.8 MB (70811091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a294f3f5dfd677171a5e33f20528eacdd28a45fdb7ecca5c0aeb3345a6d489`  
		Last Modified: Tue, 02 Jul 2024 01:39:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:afcf9c6e22d9488cf7b9a2fdfb443c9b8b77229e5544133304dbf709d5bf7f13
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100899050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f0a47849f2dd61524955cf1971d1d9d1546c280402a997d22babd9750b3ce8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:15:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 02:15:46 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 02:15:47 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 02:15:48 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:15:48 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:15:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 02:15:49 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 02:15:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 02:15:50 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:15:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 02:15:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:19:33 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:19:35 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:19:36 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:19:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:19:36 GMT
USER varnish
# Tue, 23 Jul 2024 02:19:37 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:19:38 GMT
CMD []
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261aa3d6f91e5767731a54a44a79d81d51b826a9d3a8fbac7b5c43cadeb68f52`  
		Last Modified: Tue, 23 Jul 2024 02:25:06 GMT  
		Size: 65.6 MB (65593356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ea5dee4ebd467dc96328bee533836edc95457a05eb91361cf28341a9ecaa50`  
		Last Modified: Tue, 23 Jul 2024 02:24:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; s390x

```console
$ docker pull varnish@sha256:fd48e360aacb5e383ae21bde72ca1a44ee798e12131d09c33dfd520c73448fc4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82344167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea6db8fb1fb3dacb1a627324488913688a52483f445ba12a7f9f7777009856`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:26:30 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 02 Jul 2024 03:26:31 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 02 Jul 2024 03:26:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 02 Jul 2024 03:26:31 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 03:26:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:26:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:28:35 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 03:28:37 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:28:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:28:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:28:37 GMT
USER varnish
# Tue, 02 Jul 2024 03:28:37 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:28:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a97b7ea2be3a28ebe237bdb35d3cdd9927e9942174534b7ab93622470a80098`  
		Last Modified: Tue, 02 Jul 2024 03:32:06 GMT  
		Size: 52.7 MB (52681323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb29d185f36b2b415b543aca361fdf490f1b95b399e2851e846a51fc95bc87e`  
		Last Modified: Tue, 02 Jul 2024 03:31:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3.1-alpine`

```console
$ docker pull varnish@sha256:a379160a6dae442565f2c49eb98a15abc5de1eb8bd0809ada5227c2e48477d58
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
$ docker pull varnish@sha256:0adc1921d1d1720a0e2acb6a4e929995f941b9125740338ec9ab3f304321c96a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16607ac683a4c560af2b4b117b9141a26538ff670f13f4fc3a364525253b0f1b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:23:05 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 00:23:05 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 00:23:05 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 00:23:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 00:23:06 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 00:23:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:23:06 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:24:27 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 00:24:28 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:24:28 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:24:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:24:28 GMT
USER varnish
# Tue, 23 Jul 2024 00:24:28 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:24:28 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83326aa66c31fadc8458f81f1864bd04c8b4c60081de4a49b74922c676d635c9`  
		Last Modified: Tue, 23 Jul 2024 00:26:03 GMT  
		Size: 69.6 MB (69561252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd4e5390f3d7cb29efe85bdd5ede79a3d86d2b91d9ecc9d022cb71611732890`  
		Last Modified: Tue, 23 Jul 2024 00:25:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7324d024edaf8bd09443e2bfafb5d288c078cd624349d08d9f22be26ab1d7c82
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57175436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a3d615fde91caf8c56472ecad9793bb874dc968fb6bdd989c215dc21d6e0f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:31:07 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 01:31:07 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 01:31:07 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 01:31:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:31:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:31:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 01:31:08 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 01:31:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 01:31:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 01:31:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:31:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:32:47 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:32:48 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:32:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:32:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:32:49 GMT
USER varnish
# Tue, 23 Jul 2024 01:32:49 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:32:49 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f6babe1551ab9ea2b7cfc585c356c4edae5f09f5a1ccf5fa70285301eb80`  
		Last Modified: Tue, 23 Jul 2024 01:34:13 GMT  
		Size: 54.2 MB (54247835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47fb0a3f15390b7abe7011284acb4e7fd4f7a1fa4398d9637269502dc2d70e1`  
		Last Modified: Tue, 23 Jul 2024 01:34:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:62789f930de4b24b5a49321c8ebdc3d6dfd0736719fadf1758b0342649e47871
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69688585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f934a0bd73c2f559fd959036b280a0ae21eae9bfbbec5c49a1ced6b90aea4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:40:04 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 02:40:04 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 02:40:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 02:40:05 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:40:05 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:40:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:41:14 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:41:14 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:41:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:41:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:41:14 GMT
USER varnish
# Tue, 23 Jul 2024 02:41:14 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:41:14 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f7b7f792e9ab0691612c5cc4462b434b6a3430557c497e375f9e1df0b5b98`  
		Last Modified: Tue, 23 Jul 2024 02:42:34 GMT  
		Size: 66.3 MB (66329632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191b9d3aecee2d005b4c90e24d361a83822606192e1fefa21118026139a2244`  
		Last Modified: Tue, 23 Jul 2024 02:42:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:90e0591def8ee13145f21b5daa90c5ef6bbbdbdf75853b978fd6781315b5caca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75010016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e96aa01f1d1a0d2054c348a13f4171bdbddc68288b25a4a17279ffebe1cb02b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:34:07 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 02:34:07 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 02:34:07 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 02:34:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:34:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:34:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 02:34:08 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 02:34:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 02:34:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:34:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:34:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:36:05 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:36:06 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:36:06 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:36:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:36:06 GMT
USER varnish
# Tue, 23 Jul 2024 02:36:07 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:36:07 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dac172d995b3618699d65633ad737f356c1ee1615ed90d167fe55bc0ede7dc`  
		Last Modified: Tue, 23 Jul 2024 02:37:46 GMT  
		Size: 71.8 MB (71756918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c596726176897bfbc5e1187c5feb0dbcca7befe485f468f33f16900272a18c19`  
		Last Modified: Tue, 23 Jul 2024 02:37:33 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:830afd90dff1a8c9b4aa1352b9c85ece58fd053ce8dff14309e101affe558ad0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70493238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d98a12aca2c2a82d469aba2c55840b7e23d7b0c1c1feeb5954eefd5507bbe8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:58:13 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Mon, 22 Jul 2024 23:58:13 GMT
ARG VARNISH_VERSION=7.3.1
# Mon, 22 Jul 2024 23:58:14 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Mon, 22 Jul 2024 23:58:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Mon, 22 Jul 2024 23:58:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Mon, 22 Jul 2024 23:58:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Mon, 22 Jul 2024 23:58:15 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Mon, 22 Jul 2024 23:58:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Mon, 22 Jul 2024 23:58:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Mon, 22 Jul 2024 23:58:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:58:16 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:59:33 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Mon, 22 Jul 2024 23:59:35 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:59:36 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:59:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:59:36 GMT
USER varnish
# Mon, 22 Jul 2024 23:59:36 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:59:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b2137ef36fe0bb86ba613c917d08339e19a324d7daa6eb3b6fb32870c8e504`  
		Last Modified: Tue, 23 Jul 2024 00:01:25 GMT  
		Size: 67.1 MB (67129638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a486144facf2ca024b10033d6e95cdc74facb2e458be54c098ed14ad0f336325`  
		Last Modified: Tue, 23 Jul 2024 00:01:15 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:31af442f5488b1f91a18328914449a93cf1451a716977d9cecc8f401c5a0f240
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64885502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b312cbd3c4bcb02ffa1af91db33e071fd3d6c2a4667ee0cf4a828b85b092c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:11:53 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 23 Jul 2024 01:11:53 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 23 Jul 2024 01:11:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 23 Jul 2024 01:11:53 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 01:11:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:11:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:13:14 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:13:16 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:13:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:13:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:13:17 GMT
USER varnish
# Tue, 23 Jul 2024 01:13:17 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:13:17 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5647f1c4c5339269d6f8beb83d37eaede42d4814019c3763d4467d4ba4d2402`  
		Last Modified: Tue, 23 Jul 2024 01:14:43 GMT  
		Size: 61.6 MB (61631930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a040b2bc0129a07fb0b698b4897dc3fc4a9501f221926a878282037b5987b36`  
		Last Modified: Tue, 23 Jul 2024 01:14:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4`

```console
$ docker pull varnish@sha256:5d530300a67f49028a8c18f6594c0df7ae4ba8cc75f9e207dca1b7c716e14b93
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
$ docker pull varnish@sha256:37d1ea00fcf52fdfb5b228053837545340672854a4b7dd4606d9d96adc5ca12e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134753494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7d06ba279ae2c10547844ab1808d6a20433302743582cf112afce5a4f1bedd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:56:07 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:56:07 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:56:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:56:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:56:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:58:40 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:58:41 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:58:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:58:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:58:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:58:42 GMT
USER varnish
# Tue, 02 Jul 2024 04:58:42 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566c8207791dedf3cf2fabd31800137df06433f4cba49cbb4ed9347b7e968016`  
		Last Modified: Tue, 02 Jul 2024 05:09:12 GMT  
		Size: 105.6 MB (105625204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42777929956d21d20e906e63c3ba3cd63456bd6bbb8f22bc0872ce9d1751eae1`  
		Last Modified: Tue, 02 Jul 2024 05:08:58 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6f80adf2bdd552cecb9f53beb70f3f5d7fc40005a3e6d401872f0e663294`  
		Last Modified: Tue, 02 Jul 2024 05:08:58 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; arm variant v7

```console
$ docker pull varnish@sha256:da0f5f1f8d0780b6bdc532f6eb5f5e19bade34a56388d538123a40233981021b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105006912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c825ef849dcdf5eb5b8e600e94e950b7370bc2f2871ba65768602c0c95d5745`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:15:57 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:15:58 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:15:58 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:15:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:18:22 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:18:23 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:18:23 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:18:23 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:18:24 GMT
USER varnish
# Tue, 02 Jul 2024 04:18:24 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:18:24 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e593b868ecc81ea854f53f4203520e212ec48e0ebc0a66a3b038442888dd855d`  
		Last Modified: Tue, 02 Jul 2024 04:28:37 GMT  
		Size: 80.3 MB (80286730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a775be51a6ee113268f6cafefb62c1fb81d5c7b9dcb4ee50d01cd16faa6c5d`  
		Last Modified: Tue, 02 Jul 2024 04:28:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a8d356d15205b57b447d216aca09fc08292c11f03463fd15db5938abedc0b`  
		Last Modified: Tue, 02 Jul 2024 04:28:25 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a501bc6a04026e50e398c964eeeb51b23516235bf1a364b4f64278a6bbc9e99b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129240869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d99c669f1ceed553ea0eeb32605f54a52c544620b53c55cfd2d0e4f801d2fd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:14:46 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:14:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:14:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:14:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:16:58 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:17:00 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:17:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:17:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:17:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:17:00 GMT
USER varnish
# Tue, 02 Jul 2024 04:17:00 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:17:00 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8bc01a8a92806672a3bfb149055600e15dc2ebba3247d37c6c11ed4c8cdad`  
		Last Modified: Tue, 02 Jul 2024 04:25:48 GMT  
		Size: 100.1 MB (100082293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3db704216eba227d8273c192ec346e358193854ae6ac4c3ba416b573c2d190`  
		Last Modified: Tue, 02 Jul 2024 04:25:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4b69b5d1eaeadd1cfacffbc26e1e64d2934bfa22754cb5f9dd31d87d9de9d8`  
		Last Modified: Tue, 02 Jul 2024 04:25:36 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; 386

```console
$ docker pull varnish@sha256:cfb7e07dbe578ce715c8397200534fdebd68d60368ab76c2090ca05e261cc639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131926704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a36699d08e55346abcda2529970f40066c0f1093e983f5b9b816b8dc8545d00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 01:22:54 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 01:22:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:22:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:22:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:26:08 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:26:10 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:26:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:26:10 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:26:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:26:11 GMT
USER varnish
# Tue, 02 Jul 2024 01:26:11 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:26:11 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022680d52f70894469d7c28d759fcb6cc1af7ddb0e1eb97ceeac9c4242b9b3fe`  
		Last Modified: Tue, 02 Jul 2024 01:38:31 GMT  
		Size: 101.8 MB (101780415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8641c300252521fa15bfb445ed8134c6bf7b6a5c99e481d656fbc3b9707b28`  
		Last Modified: Tue, 02 Jul 2024 01:38:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf14b6ded3b7274948e430a9c35ca995e6d2cd0154738ee27a50002b37a9870`  
		Last Modified: Tue, 02 Jul 2024 01:38:11 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; ppc64le

```console
$ docker pull varnish@sha256:1def881556ab48080e777d8f6d22ec19ada032a5dba828b2e71ef7a4a35d6cba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137693599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b0ecf3467a4156469bfbe6cdd1a525727f67197b668e92e1d91a7bd814b23d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:03:25 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:03:25 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:03:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:03:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:03:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 02:03:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:07:30 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:07:34 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:07:34 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:07:35 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:07:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:07:36 GMT
USER varnish
# Tue, 23 Jul 2024 02:07:36 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:07:36 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7a2c43b896069ccdf5ea950ed605b4a0b958b8faa94693fd918248ded3d47f`  
		Last Modified: Tue, 23 Jul 2024 02:24:04 GMT  
		Size: 104.6 MB (104569312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2846c911c8a8733da1790dbc02bb73238b1616c8613df2bf297469ff2f05ad`  
		Last Modified: Tue, 23 Jul 2024 02:23:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805c71dead9d8bfb40fe7c28613a776ad2fe4ff1be6cc73b26964efcf7b9006d`  
		Last Modified: Tue, 23 Jul 2024 02:23:47 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; s390x

```console
$ docker pull varnish@sha256:548459afd525a54eb52e7e894a1b0fe1b53ce0ea30b41df24454b6d125f7f87d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112340105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078de114c46737c3e9118e346a9f2586976adc8f417687f251b9aeecef31a57`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:15:39 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 03:18:54 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 03:18:54 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 03:18:54 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 03:18:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 03:18:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:18:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:21:09 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 03:21:12 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:21:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:21:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 03:21:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:21:12 GMT
USER varnish
# Tue, 02 Jul 2024 03:21:12 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:21:13 GMT
CMD []
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc3c811cb63b01096d259387bd31a4ceaaa31de3560294006525cd38de3a9dd`  
		Last Modified: Tue, 02 Jul 2024 03:31:22 GMT  
		Size: 84.8 MB (84848004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa4ddfaa7c86e7691b9de08dd07300c2163874027a9df0dd78a6a0d12f1485`  
		Last Modified: Tue, 02 Jul 2024 03:31:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e15199fe8065c4a7ec6991a0150e8988673234bd59b0a3618ad93b8f25e203c`  
		Last Modified: Tue, 02 Jul 2024 03:31:10 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4-alpine`

```console
$ docker pull varnish@sha256:704092e07547d966900898f7d71e3fc1e11cf062cdaff09659b92ec5677fccf8
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
$ docker pull varnish@sha256:627cff1fdecac0904f7d6f767ade41ed354697530014be0c02aa28ded143af7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2298b48360e011b725d026b4a28a533c54c78b5046af35617dd90790c0116ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 00:19:39 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:19:40 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 00:19:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 00:19:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:19:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:19:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:21:02 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 00:21:02 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:21:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:21:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:21:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:21:03 GMT
USER varnish
# Tue, 23 Jul 2024 00:21:03 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:21:03 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62d6dfb9e82e0a7c05c07cb2ddbb6063b9e223093be1be57f917f648c389df5`  
		Last Modified: Tue, 23 Jul 2024 00:25:29 GMT  
		Size: 69.7 MB (69703561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108ea953524427a74b8e4003df1d92066bb9b65a7689df697de4e034192fcf3`  
		Last Modified: Tue, 23 Jul 2024 00:25:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d819bb73a613ed5355434fdf1b76ea822d24a868b54af7cb7eb914c2f5201cea`  
		Last Modified: Tue, 23 Jul 2024 00:25:20 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3c26c259ff513521c809b737cf7c4db2f45e0fcb2fe5982b89e4e53d95d3239b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57327047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab3561e54c063f20cf3e0ac756eaf3a39d6ce572a2866b3b2c23c50e40b12e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 01:27:30 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:27:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:27:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:27:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:27:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:29:07 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:29:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:29:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:29:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:29:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:29:08 GMT
USER varnish
# Tue, 23 Jul 2024 01:29:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:29:08 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffefcdaabd64405cde52b5bfc485da2f6f6b676c13cb39b8f6522fc9d1594a19`  
		Last Modified: Tue, 23 Jul 2024 01:33:44 GMT  
		Size: 54.4 MB (54397919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb267507ecb05fc645190517c37cd1b296f9af2e118c8439d2b14c5d965a07d`  
		Last Modified: Tue, 23 Jul 2024 01:33:38 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f8ed2e6566df6eb66c3ee86b80ca98f5a24ebf7d0fa61542db60a9612c8e`  
		Last Modified: Tue, 23 Jul 2024 01:33:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:323ff4d1330b61943f18d1d0ff9794ad7acf045e943c539fc1249bf1211a5cbc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69826933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ed7787250fde0fffc58cfc97de470ee64b113d554003c768f086e70eeae4f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:37:13 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:37:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:37:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:37:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:38:23 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:38:24 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:38:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:38:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:38:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:38:24 GMT
USER varnish
# Tue, 23 Jul 2024 02:38:24 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:38:24 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c75650c9e9beb0a0b55b6521bf2c00e229b25ce1da391bc2b51c20034f7715`  
		Last Modified: Tue, 23 Jul 2024 02:42:05 GMT  
		Size: 66.5 MB (66466452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782e41c252bdd7b99370d9bceb9a0a4e626667831c25eedb78975fbcd9812466`  
		Last Modified: Tue, 23 Jul 2024 02:41:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caf1aa65ec481deb40e5763e6b430a369311339764cddce0cea51b02ac40137`  
		Last Modified: Tue, 23 Jul 2024 02:42:00 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; 386

```console
$ docker pull varnish@sha256:93d18ad0c95d0deb3c906a588cf6d311db49951f2fdb9abb68da62fac415ac57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75146245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6926482de52318c54726ad8e2fa23c44786aab22c8e75184a9a17dcc84033e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:29:31 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:29:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:29:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:29:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:31:30 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:31:31 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:31:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:31:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:31:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:31:31 GMT
USER varnish
# Tue, 23 Jul 2024 02:31:31 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:31:31 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1b4cbd7f1a5cf901465ed58deb6357f76f9211644022ce88c5d5920d6d167a`  
		Last Modified: Tue, 23 Jul 2024 02:37:05 GMT  
		Size: 71.9 MB (71891627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a34a55e7f14e39e8e2cbda4ef23cf40ed97fb7a1d7167cec8d6b89300806a3`  
		Last Modified: Tue, 23 Jul 2024 02:36:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ffec8c83931eceb1a10310c300cf14063872ece7746b7627ec425ce98b8cc6`  
		Last Modified: Tue, 23 Jul 2024 02:36:53 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ccd5208b46c61c09985bf6a62cfc23e359dc4a735ca89e66eb6d75edd99be95a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70649093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7db6c58c9661a31f4581894a4ed80f1cd031b1ad69a58b3c55d3a93677e776`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:54:46 GMT
ARG VARNISH_VERSION=7.4.3
# Mon, 22 Jul 2024 23:54:46 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Mon, 22 Jul 2024 23:54:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Mon, 22 Jul 2024 23:54:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Mon, 22 Jul 2024 23:54:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:54:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:54:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:56:06 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Mon, 22 Jul 2024 23:56:08 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:56:09 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:56:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:56:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:56:10 GMT
USER varnish
# Mon, 22 Jul 2024 23:56:10 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c497a12642e96290baee7f966db9cb2744473cf6812498312cd099d9e4c788`  
		Last Modified: Tue, 23 Jul 2024 00:00:48 GMT  
		Size: 67.3 MB (67283965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad1c1f35306fb4d2e94bd212b097e210af7aa489f14f474981e4bd0966f8eb`  
		Last Modified: Tue, 23 Jul 2024 00:00:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e80c54b9ae6306112403d683f5c81013cccd2f3d65c26bdde78a3f274b16f6`  
		Last Modified: Tue, 23 Jul 2024 00:00:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:26e24c18193128808a01eb0041756acf7a3993a707f2ae9a834b39c730552a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65025041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290c0fef2dba059a5b8af56803d0a87ebad56ad7fe4f62f4a1860e357865ce0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 01:08:20 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:08:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:08:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:08:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:08:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:09:45 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:09:47 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:09:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:09:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:09:48 GMT
USER varnish
# Tue, 23 Jul 2024 01:09:48 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e066951adfe18da6dc61367ee5810bf1308f7cb284457d8b0f0bb7fb5213cbd`  
		Last Modified: Tue, 23 Jul 2024 01:14:15 GMT  
		Size: 61.8 MB (61769943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc0b53e844c962ccc1922fb4fa3f8d4cf4c33abae2d8262e874e26d62c77cbd`  
		Last Modified: Tue, 23 Jul 2024 01:14:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010fd03a1011d817ebf0b5574407ede3696fcf1623c3422b76eac7d0e48844c7`  
		Last Modified: Tue, 23 Jul 2024 01:14:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.2`

```console
$ docker pull varnish@sha256:41e8fb8e54421138e7c433805816a49d6a3b115ea164034aae6b676fd440e483
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
$ docker pull varnish@sha256:26e05b3470a690d11d996c8ffdbb560caf44d3ae42a710062df51b3b584a0085
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134758593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46ecfb8f9cbfa8744b5aef3b496cb367bc7eab720d3a860b4358c06eb4473b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 05:00:58 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 02 Jul 2024 05:00:58 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 02 Jul 2024 05:00:58 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 05:00:58 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 05:00:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 05:00:58 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 05:00:58 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 05:00:59 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 05:00:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 05:00:59 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:03:31 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 05:03:31 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:03:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:03:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:03:32 GMT
USER varnish
# Tue, 02 Jul 2024 05:03:32 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:03:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd838a2af1f4d9cc3eed76ed43265e7cec41e5cffd673ed680b81945086e698`  
		Last Modified: Tue, 02 Jul 2024 05:09:55 GMT  
		Size: 105.6 MB (105631823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de63dd9528717489f1e5eb1a0868dc21ca684cdb92246bc76b7575a1aa30124`  
		Last Modified: Tue, 02 Jul 2024 05:09:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; arm variant v7

```console
$ docker pull varnish@sha256:03853e07e0d1b1f8acbb30d0c08fe5f2e718c471a5ed1e467618f84eca74b589
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104983081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d102a9d8b2f361592223fd73e5225f69ee9173db2985065b7f0f773b4260bc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:20:30 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 02 Jul 2024 04:20:30 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 02 Jul 2024 04:20:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:20:30 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:20:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:20:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:20:30 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:20:31 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 04:20:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:20:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:22:54 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 04:22:55 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:22:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:22:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:22:56 GMT
USER varnish
# Tue, 02 Jul 2024 04:22:56 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:22:56 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4087d33794c8f9672b85d0e273c55632bd0bfa539cf03aedabe64d61e7ad114d`  
		Last Modified: Tue, 02 Jul 2024 04:29:14 GMT  
		Size: 80.3 MB (80264419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cf7a187029fcab2e76811651d1fc570ea1edf13eb7cdaaf807d74503858e4d`  
		Last Modified: Tue, 02 Jul 2024 04:29:03 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a88c34413807cc487a341d8817c685330d58091ddb437f30abadf245f96d4714
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129248317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a5f30b5649ecc33c87bb61cdd6d5c9f172c2f7f2555b8957e19626dd6d2dc7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:18:48 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 02 Jul 2024 04:18:48 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 02 Jul 2024 04:18:48 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:18:48 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:18:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:18:49 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:18:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:18:49 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 04:18:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:18:49 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:20:59 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 04:21:00 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:21:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:21:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:21:00 GMT
USER varnish
# Tue, 02 Jul 2024 04:21:00 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:21:00 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6df3fd0245b922eb944da3439f9885ad7afcadf53651e7a2022c67a524414cd`  
		Last Modified: Tue, 02 Jul 2024 04:26:25 GMT  
		Size: 100.1 MB (100091262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbdc653cf6e096d5108093ae11ec30820030785cdf03a998eff7c949eec234f`  
		Last Modified: Tue, 02 Jul 2024 04:26:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; 386

```console
$ docker pull varnish@sha256:c1919810111584be0312c96572ad17ce05a2a1b0566fd381a486f531fb8bef16
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131883178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98acc5a478436b84e8a9079d0cbaa5f236798e52124c178b5fe53640b316d187`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:28:42 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 02 Jul 2024 01:28:42 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 02 Jul 2024 01:28:42 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 01:28:42 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 01:28:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:28:42 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 01:28:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 01:28:42 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 01:28:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:28:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:31:55 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 01:31:57 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:31:57 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:31:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:31:57 GMT
USER varnish
# Tue, 02 Jul 2024 01:31:58 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:31:58 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e84ae7e387637c1660ede9ff4b4ca011fc9ee91e4aeaeb38f9513014d7b558`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 101.7 MB (101738411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141ffd01f90df11a7e87c54c52670c627ae08bd0928bbf31c73d8b78450bd0e3`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; ppc64le

```console
$ docker pull varnish@sha256:913cef1503db81c00f57e3f4e34b2cc73e08057a1c1ea946eaee5518767f8b93
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137675356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3f8fd26b356b088b94c7684e74dbd1f221f6d1a82fe2d213d80a6d65fd7a6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:11:18 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 23 Jul 2024 02:11:18 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 23 Jul 2024 02:11:18 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:11:19 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:11:19 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:11:20 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:11:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:11:21 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:11:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 02:11:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:15:34 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:15:38 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:15:38 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:15:39 GMT
USER varnish
# Tue, 23 Jul 2024 02:15:40 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:15:40 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d989acf7bf1c2ae69cadeaaa2559a597f9a3fbce802223c6d03de9ff28a1485`  
		Last Modified: Tue, 23 Jul 2024 02:24:50 GMT  
		Size: 104.6 MB (104552590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a838caf99f02351279db4f2f51820712a9e98db11596b7cde5da9157771e13de`  
		Last Modified: Tue, 23 Jul 2024 02:24:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; s390x

```console
$ docker pull varnish@sha256:d1e4fc7ce4de065d1c7d331aa6fe8aa09cf052768f5281783f3108d2d9254239
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112331806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4afbb50060d3cdec1ecba82c970efb4a2a320d26c4b2b9a1a5a30da67e72914`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:15:39 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 03:23:46 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 02 Jul 2024 03:23:46 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 02 Jul 2024 03:23:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 03:23:46 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 03:23:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 03:23:47 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 03:23:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 03:23:47 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 02 Jul 2024 03:23:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:23:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:25:59 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 02 Jul 2024 03:26:02 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:26:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:26:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:26:02 GMT
USER varnish
# Tue, 02 Jul 2024 03:26:03 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:26:03 GMT
CMD []
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3430d9e5ca3955e89e94d7fc4029ae9e30a7b038225c321feb4469b9bfba1e0`  
		Last Modified: Tue, 02 Jul 2024 03:31:55 GMT  
		Size: 84.8 MB (84841225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbea4665c400f0e7f5138a5b4435fcbfe5578c86a30ec4d968338db26d91562`  
		Last Modified: Tue, 02 Jul 2024 03:31:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.2-alpine`

```console
$ docker pull varnish@sha256:ceb31f28ec8aeffce2b513a3de65641fca0a5d6fddb8e17c1f16e01e84e41877
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
$ docker pull varnish@sha256:686887a9d4b2ce8e192db0474c8db2bd5ed30f7dae2fb44e9c33265e6e28aab2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73107924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69f2e7ce4b3d18a9c1f40572435f7440a73d7c92a18c9f4d0fe172dd08a0b18`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:21:23 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 23 Jul 2024 00:21:23 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 23 Jul 2024 00:21:23 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 00:21:23 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 00:21:23 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:21:23 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 00:21:24 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 00:21:24 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 00:21:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:21:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:22:46 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 00:22:47 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:22:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:22:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:22:47 GMT
USER varnish
# Tue, 23 Jul 2024 00:22:47 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:22:47 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd1d101ca5d8b2322c9732ba9779ff880fe6d3e0c90128ae42ebca767a7f252`  
		Last Modified: Tue, 23 Jul 2024 00:25:48 GMT  
		Size: 69.7 MB (69688388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7312bc94a15f12cfd34449bd2fa5a04beff5a15345eade57db1ab31ed3ffbb5`  
		Last Modified: Tue, 23 Jul 2024 00:25:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:175be4e4297d9512a42cabb6be7f5d96a56dc9018ce7c14b73f11050562439a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57310063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7a622bfb2355d8b8694a7186fceba6b86e8f104d8aac91c9d9b4e63ac567bb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:29:28 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 23 Jul 2024 01:29:28 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 23 Jul 2024 01:29:28 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:29:28 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:29:28 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:29:29 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:29:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:29:29 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 01:29:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:29:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:30:59 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:30:59 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:30:59 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:31:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:31:00 GMT
USER varnish
# Tue, 23 Jul 2024 01:31:00 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:31:00 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376cf34c6c8e740948632b07b58162da882dc20410bb2a85880d994b2c439948`  
		Last Modified: Tue, 23 Jul 2024 01:34:01 GMT  
		Size: 54.4 MB (54382461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d19eb54b414dc05217a118671973be0bcb22bc255ad7d4ae4296e60c59ce46`  
		Last Modified: Tue, 23 Jul 2024 01:33:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0c1b8d9b0a33622830a8a5d210dc7492094e33e7600b940f3ab60919646954a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69817791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1884c33e95197cc76a6431c3f09e58cdc7c15157b0eaed1ce2cfe40de70a7d6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:38:39 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 23 Jul 2024 02:38:39 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 23 Jul 2024 02:38:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:38:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:38:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:38:40 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:38:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:38:40 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:38:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:38:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:39:50 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:39:50 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:39:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:39:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:39:50 GMT
USER varnish
# Tue, 23 Jul 2024 02:39:50 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:39:51 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5496db91850f0c77a237d302dd3fd00c6ae0a1e46fb9611f06325e3f3fceb24b`  
		Last Modified: Tue, 23 Jul 2024 02:42:21 GMT  
		Size: 66.5 MB (66458836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306c249bce728e0e972319346c42954a25412c6fe8659660a847e55e41b25299`  
		Last Modified: Tue, 23 Jul 2024 02:42:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; 386

```console
$ docker pull varnish@sha256:f81f9ebf3103cbacfc2884b71d98f1453794a99fd8f7c5d7ef0b9592c0bbad7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75130575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4924885309741f594bf420ccf840bea5dd2a1f72bf3b960d1505c3fa7dafbe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:31:42 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 23 Jul 2024 02:31:42 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 23 Jul 2024 02:31:42 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:31:43 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:31:43 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:31:43 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:31:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:31:43 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 02:31:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:31:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:33:51 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:33:52 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:33:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:33:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:33:52 GMT
USER varnish
# Tue, 23 Jul 2024 02:33:52 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:33:52 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc34cfdc24ba23a43801baa29fbd6a0204048a9bafb25e9ba018329c9412c38`  
		Last Modified: Tue, 23 Jul 2024 02:37:27 GMT  
		Size: 71.9 MB (71877476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de5036c4c6d311bcfb1ae18fb10bcdc3035b4644196d5f914e78dccf7b01c82`  
		Last Modified: Tue, 23 Jul 2024 02:37:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:49f73d5bcbaf66d0d4af7dbe68b2fd7ae2af7696c7a0d1842e5e64c1088f1ca5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70625044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8401d7163373d23e2fac7b533d6f0a81cd45c58f4ca6f74e35e7b1f2ac6797e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:56:30 GMT
ARG VARNISH_VERSION=7.4.2
# Mon, 22 Jul 2024 23:56:31 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Mon, 22 Jul 2024 23:56:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Mon, 22 Jul 2024 23:56:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Mon, 22 Jul 2024 23:56:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:56:32 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Mon, 22 Jul 2024 23:56:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Mon, 22 Jul 2024 23:56:33 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Mon, 22 Jul 2024 23:56:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:56:33 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:57:50 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Mon, 22 Jul 2024 23:57:53 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:57:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:57:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:57:53 GMT
USER varnish
# Mon, 22 Jul 2024 23:57:54 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:57:54 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae943bb741230201a48038dbeff398081068c31297eb98b3d2e9882a4f82fb41`  
		Last Modified: Tue, 23 Jul 2024 00:01:08 GMT  
		Size: 67.3 MB (67261443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2736d1bcd929c6b81373c29aa9a94ff42235cfd8eef25330ffb9aa44ef24f80d`  
		Last Modified: Tue, 23 Jul 2024 00:00:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:59482c5a5daf61cc879fcf1eddb04259e6ffe2380337714dec7987e795bd161f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65007500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdda0c5e4b5c482d8147172342e99768d82a8015407aa902d6e36dd6a91ce6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:10:09 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 23 Jul 2024 01:10:10 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 23 Jul 2024 01:10:10 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:10:10 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:10:10 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:10:10 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:10:10 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:10:10 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 23 Jul 2024 01:10:10 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:10:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:11:37 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:11:39 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:11:39 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:11:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:11:39 GMT
USER varnish
# Tue, 23 Jul 2024 01:11:39 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:11:39 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51253b85e19b001bd5597cce07a2f37ab36a0082b9ccccb43e327ab85b87c8d1`  
		Last Modified: Tue, 23 Jul 2024 01:14:31 GMT  
		Size: 61.8 MB (61753930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bfbfe0413f2c5e448f041406199269846eff28f4e6269685cc313a958bbc99`  
		Last Modified: Tue, 23 Jul 2024 01:14:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.3`

```console
$ docker pull varnish@sha256:ec9c15c727e5c68ee57d4b79d33125c7adf7b5d9e480547ea5f11be00f38f41a
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
$ docker pull varnish@sha256:37d1ea00fcf52fdfb5b228053837545340672854a4b7dd4606d9d96adc5ca12e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134753494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7d06ba279ae2c10547844ab1808d6a20433302743582cf112afce5a4f1bedd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:56:07 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:56:07 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:56:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:56:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:56:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:58:40 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:58:41 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:58:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:58:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:58:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:58:42 GMT
USER varnish
# Tue, 02 Jul 2024 04:58:42 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566c8207791dedf3cf2fabd31800137df06433f4cba49cbb4ed9347b7e968016`  
		Last Modified: Tue, 02 Jul 2024 05:09:12 GMT  
		Size: 105.6 MB (105625204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42777929956d21d20e906e63c3ba3cd63456bd6bbb8f22bc0872ce9d1751eae1`  
		Last Modified: Tue, 02 Jul 2024 05:08:58 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6f80adf2bdd552cecb9f53beb70f3f5d7fc40005a3e6d401872f0e663294`  
		Last Modified: Tue, 02 Jul 2024 05:08:58 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:da0f5f1f8d0780b6bdc532f6eb5f5e19bade34a56388d538123a40233981021b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105006912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c825ef849dcdf5eb5b8e600e94e950b7370bc2f2871ba65768602c0c95d5745`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:15:57 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:15:58 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:15:58 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:15:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:18:22 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:18:23 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:18:23 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:18:23 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:18:24 GMT
USER varnish
# Tue, 02 Jul 2024 04:18:24 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:18:24 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e593b868ecc81ea854f53f4203520e212ec48e0ebc0a66a3b038442888dd855d`  
		Last Modified: Tue, 02 Jul 2024 04:28:37 GMT  
		Size: 80.3 MB (80286730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a775be51a6ee113268f6cafefb62c1fb81d5c7b9dcb4ee50d01cd16faa6c5d`  
		Last Modified: Tue, 02 Jul 2024 04:28:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a8d356d15205b57b447d216aca09fc08292c11f03463fd15db5938abedc0b`  
		Last Modified: Tue, 02 Jul 2024 04:28:25 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a501bc6a04026e50e398c964eeeb51b23516235bf1a364b4f64278a6bbc9e99b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129240869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d99c669f1ceed553ea0eeb32605f54a52c544620b53c55cfd2d0e4f801d2fd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:14:46 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:14:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:14:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:14:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:16:58 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:17:00 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:17:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:17:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:17:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:17:00 GMT
USER varnish
# Tue, 02 Jul 2024 04:17:00 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:17:00 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8bc01a8a92806672a3bfb149055600e15dc2ebba3247d37c6c11ed4c8cdad`  
		Last Modified: Tue, 02 Jul 2024 04:25:48 GMT  
		Size: 100.1 MB (100082293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3db704216eba227d8273c192ec346e358193854ae6ac4c3ba416b573c2d190`  
		Last Modified: Tue, 02 Jul 2024 04:25:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4b69b5d1eaeadd1cfacffbc26e1e64d2934bfa22754cb5f9dd31d87d9de9d8`  
		Last Modified: Tue, 02 Jul 2024 04:25:36 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; 386

```console
$ docker pull varnish@sha256:cfb7e07dbe578ce715c8397200534fdebd68d60368ab76c2090ca05e261cc639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131926704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a36699d08e55346abcda2529970f40066c0f1093e983f5b9b816b8dc8545d00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 01:22:54 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 01:22:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:22:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:22:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:26:08 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:26:10 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:26:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:26:10 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:26:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:26:11 GMT
USER varnish
# Tue, 02 Jul 2024 01:26:11 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:26:11 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022680d52f70894469d7c28d759fcb6cc1af7ddb0e1eb97ceeac9c4242b9b3fe`  
		Last Modified: Tue, 02 Jul 2024 01:38:31 GMT  
		Size: 101.8 MB (101780415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8641c300252521fa15bfb445ed8134c6bf7b6a5c99e481d656fbc3b9707b28`  
		Last Modified: Tue, 02 Jul 2024 01:38:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf14b6ded3b7274948e430a9c35ca995e6d2cd0154738ee27a50002b37a9870`  
		Last Modified: Tue, 02 Jul 2024 01:38:11 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:1def881556ab48080e777d8f6d22ec19ada032a5dba828b2e71ef7a4a35d6cba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137693599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b0ecf3467a4156469bfbe6cdd1a525727f67197b668e92e1d91a7bd814b23d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:03:25 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:03:25 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:03:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:03:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:03:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 02:03:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:07:30 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:07:34 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:07:34 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:07:35 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:07:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:07:36 GMT
USER varnish
# Tue, 23 Jul 2024 02:07:36 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:07:36 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7a2c43b896069ccdf5ea950ed605b4a0b958b8faa94693fd918248ded3d47f`  
		Last Modified: Tue, 23 Jul 2024 02:24:04 GMT  
		Size: 104.6 MB (104569312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2846c911c8a8733da1790dbc02bb73238b1616c8613df2bf297469ff2f05ad`  
		Last Modified: Tue, 23 Jul 2024 02:23:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805c71dead9d8bfb40fe7c28613a776ad2fe4ff1be6cc73b26964efcf7b9006d`  
		Last Modified: Tue, 23 Jul 2024 02:23:47 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; s390x

```console
$ docker pull varnish@sha256:30716af5f9801c41eb4e88c582f6a0dadcfca99fe37fe18ce40a95502546da20
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112341967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f81c5d48f143ec80be8aee589c2c509e53a835974324335301fdf4ba58376e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 02:27:49 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Tue, 23 Jul 2024 02:27:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:25:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 03:28:02 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 03:28:02 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 03:28:03 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 03:28:03 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 03:28:03 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 03:28:03 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 03:28:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 03:28:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 03:28:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 03:28:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 03:30:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 03:30:22 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 03:30:22 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:30:22 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 03:30:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 03:30:22 GMT
USER varnish
# Tue, 23 Jul 2024 03:30:22 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 03:30:22 GMT
CMD []
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371587b8ae78b543a2c4c916b3d40ef4d50bf2fb1920ba1d79c6ba71adaa77ea`  
		Last Modified: Tue, 23 Jul 2024 03:40:19 GMT  
		Size: 84.8 MB (84849856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d16ad0c3467e5c32dcd2980913dfeacbeee981e8d023429b638bc2654eba7fe`  
		Last Modified: Tue, 23 Jul 2024 03:40:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987d5ec6ae7b790334d7fb5fb4e241f1fd9715234c61daf2be8e81ec11e749e7`  
		Last Modified: Tue, 23 Jul 2024 03:40:07 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.3-alpine`

```console
$ docker pull varnish@sha256:704092e07547d966900898f7d71e3fc1e11cf062cdaff09659b92ec5677fccf8
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
$ docker pull varnish@sha256:627cff1fdecac0904f7d6f767ade41ed354697530014be0c02aa28ded143af7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2298b48360e011b725d026b4a28a533c54c78b5046af35617dd90790c0116ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 00:19:39 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:19:40 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 00:19:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 00:19:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:19:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:19:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:21:02 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 00:21:02 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:21:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:21:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:21:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:21:03 GMT
USER varnish
# Tue, 23 Jul 2024 00:21:03 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:21:03 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62d6dfb9e82e0a7c05c07cb2ddbb6063b9e223093be1be57f917f648c389df5`  
		Last Modified: Tue, 23 Jul 2024 00:25:29 GMT  
		Size: 69.7 MB (69703561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108ea953524427a74b8e4003df1d92066bb9b65a7689df697de4e034192fcf3`  
		Last Modified: Tue, 23 Jul 2024 00:25:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d819bb73a613ed5355434fdf1b76ea822d24a868b54af7cb7eb914c2f5201cea`  
		Last Modified: Tue, 23 Jul 2024 00:25:20 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3c26c259ff513521c809b737cf7c4db2f45e0fcb2fe5982b89e4e53d95d3239b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57327047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab3561e54c063f20cf3e0ac756eaf3a39d6ce572a2866b3b2c23c50e40b12e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 01:27:30 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:27:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:27:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:27:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:27:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:29:07 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:29:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:29:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:29:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:29:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:29:08 GMT
USER varnish
# Tue, 23 Jul 2024 01:29:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:29:08 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffefcdaabd64405cde52b5bfc485da2f6f6b676c13cb39b8f6522fc9d1594a19`  
		Last Modified: Tue, 23 Jul 2024 01:33:44 GMT  
		Size: 54.4 MB (54397919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb267507ecb05fc645190517c37cd1b296f9af2e118c8439d2b14c5d965a07d`  
		Last Modified: Tue, 23 Jul 2024 01:33:38 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f8ed2e6566df6eb66c3ee86b80ca98f5a24ebf7d0fa61542db60a9612c8e`  
		Last Modified: Tue, 23 Jul 2024 01:33:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:323ff4d1330b61943f18d1d0ff9794ad7acf045e943c539fc1249bf1211a5cbc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69826933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ed7787250fde0fffc58cfc97de470ee64b113d554003c768f086e70eeae4f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:37:13 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:37:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:37:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:37:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:38:23 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:38:24 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:38:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:38:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:38:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:38:24 GMT
USER varnish
# Tue, 23 Jul 2024 02:38:24 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:38:24 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c75650c9e9beb0a0b55b6521bf2c00e229b25ce1da391bc2b51c20034f7715`  
		Last Modified: Tue, 23 Jul 2024 02:42:05 GMT  
		Size: 66.5 MB (66466452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782e41c252bdd7b99370d9bceb9a0a4e626667831c25eedb78975fbcd9812466`  
		Last Modified: Tue, 23 Jul 2024 02:41:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caf1aa65ec481deb40e5763e6b430a369311339764cddce0cea51b02ac40137`  
		Last Modified: Tue, 23 Jul 2024 02:42:00 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:93d18ad0c95d0deb3c906a588cf6d311db49951f2fdb9abb68da62fac415ac57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75146245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6926482de52318c54726ad8e2fa23c44786aab22c8e75184a9a17dcc84033e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:29:31 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:29:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:29:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:29:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:31:30 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:31:31 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:31:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:31:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:31:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:31:31 GMT
USER varnish
# Tue, 23 Jul 2024 02:31:31 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:31:31 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1b4cbd7f1a5cf901465ed58deb6357f76f9211644022ce88c5d5920d6d167a`  
		Last Modified: Tue, 23 Jul 2024 02:37:05 GMT  
		Size: 71.9 MB (71891627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a34a55e7f14e39e8e2cbda4ef23cf40ed97fb7a1d7167cec8d6b89300806a3`  
		Last Modified: Tue, 23 Jul 2024 02:36:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ffec8c83931eceb1a10310c300cf14063872ece7746b7627ec425ce98b8cc6`  
		Last Modified: Tue, 23 Jul 2024 02:36:53 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ccd5208b46c61c09985bf6a62cfc23e359dc4a735ca89e66eb6d75edd99be95a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70649093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7db6c58c9661a31f4581894a4ed80f1cd031b1ad69a58b3c55d3a93677e776`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:54:46 GMT
ARG VARNISH_VERSION=7.4.3
# Mon, 22 Jul 2024 23:54:46 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Mon, 22 Jul 2024 23:54:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Mon, 22 Jul 2024 23:54:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Mon, 22 Jul 2024 23:54:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:54:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:54:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:56:06 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Mon, 22 Jul 2024 23:56:08 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:56:09 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:56:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:56:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:56:10 GMT
USER varnish
# Mon, 22 Jul 2024 23:56:10 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c497a12642e96290baee7f966db9cb2744473cf6812498312cd099d9e4c788`  
		Last Modified: Tue, 23 Jul 2024 00:00:48 GMT  
		Size: 67.3 MB (67283965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad1c1f35306fb4d2e94bd212b097e210af7aa489f14f474981e4bd0966f8eb`  
		Last Modified: Tue, 23 Jul 2024 00:00:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e80c54b9ae6306112403d683f5c81013cccd2f3d65c26bdde78a3f274b16f6`  
		Last Modified: Tue, 23 Jul 2024 00:00:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:26e24c18193128808a01eb0041756acf7a3993a707f2ae9a834b39c730552a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65025041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290c0fef2dba059a5b8af56803d0a87ebad56ad7fe4f62f4a1860e357865ce0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 01:08:20 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:08:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:08:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:08:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:08:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:09:45 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:09:47 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:09:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:09:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:09:48 GMT
USER varnish
# Tue, 23 Jul 2024 01:09:48 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e066951adfe18da6dc61367ee5810bf1308f7cb284457d8b0f0bb7fb5213cbd`  
		Last Modified: Tue, 23 Jul 2024 01:14:15 GMT  
		Size: 61.8 MB (61769943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc0b53e844c962ccc1922fb4fa3f8d4cf4c33abae2d8262e874e26d62c77cbd`  
		Last Modified: Tue, 23 Jul 2024 01:14:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010fd03a1011d817ebf0b5574407ede3696fcf1623c3422b76eac7d0e48844c7`  
		Last Modified: Tue, 23 Jul 2024 01:14:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5`

```console
$ docker pull varnish@sha256:5b95c1b1eef8cd37cc12767cbf42eef26961a3a3c1a436f5ff36603065baba2c
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
$ docker pull varnish@sha256:c6245b1f63629f17d20d1d309de3f04aedf929e0a4281c8cd3a6a620daf384c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134862254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d25f7e828ba6e722bb372cb9999fd138682017e0d0b82b4b09a62257f6a9d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:53:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:56:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:56:01 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:56:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:56:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:56:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:56:01 GMT
USER varnish
# Tue, 02 Jul 2024 04:56:01 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:56:01 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16282c1add7c3baf6d62eb91f9434ef31e076bad8ac6529d2cbfd698fe683741`  
		Last Modified: Tue, 02 Jul 2024 05:08:45 GMT  
		Size: 105.7 MB (105733962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c568179d88274cbd7625ae74d29623d927c778a5f308ca67a42c6161e40344a1`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d438f5bf9894896e1ddf61c4267996ae7846e743e09b3ec47e2d3dc15054f33`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:65485dda4043010bd4ff6eb58d0b1701da60cfaedc861a70517d12eece89b467
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105116843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db62a170426bdff0051f3ec4d04b7c60e7333abe107705cfc17568b91dfa7f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:13:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:15:47 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:15:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:15:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:15:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:15:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:15:48 GMT
USER varnish
# Tue, 02 Jul 2024 04:15:48 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:15:48 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279719837527914fe9e5ff9709d81b1b0491eeed0cfb3c96ebf61511a68d10d8`  
		Last Modified: Tue, 02 Jul 2024 04:28:11 GMT  
		Size: 80.4 MB (80396664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72405d38d5b76fbbb94bd00812bb4bc48a94f476e840bdf82d60ff448ec3bafb`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3286e9b8ef98b08bbdee8bba6fca44840cf23c39848c227879d38b6f47a202c2`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:944e5e7eedff373706f516f36571fcc31e190d2b7e8693ad6528e62a23ee4b1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129339124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b778778b32af3328bcc517f80f8d47dfc7f858dedff1babf6ce45657180fa805`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:12:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:14:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:14:29 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:14:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:14:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:14:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:14:30 GMT
USER varnish
# Tue, 02 Jul 2024 04:14:30 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:14:30 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05fe21d9623c5387c391eec805dcd1526fb2ba19a3e0c4e632507c4f13e0dfd`  
		Last Modified: Tue, 02 Jul 2024 04:25:24 GMT  
		Size: 100.2 MB (100180549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d79257db29f3e1df4726e5423044d921f36494d042aca76d7b44cf787505`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3165c0b54f641e6fa1b49d6d5236759255cf0c4362f3df5b3219ffd917aa7be`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; 386

```console
$ docker pull varnish@sha256:bcaf2304278bbba8198a7fedb08acb5e6c43634378109924fccbd76a19a219f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132020835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24f1647d3dcad13568e201a9b3191c4aabe04495ecc18bada34219daac499b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 01:19:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:22:45 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:22:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:22:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:22:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:22:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:22:47 GMT
USER varnish
# Tue, 02 Jul 2024 01:22:47 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:22:48 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d32edbfc26351211befe908d30b1eada8a1223d9a90ebd1215a772c0861b2`  
		Last Modified: Tue, 02 Jul 2024 01:37:59 GMT  
		Size: 101.9 MB (101874548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdf815f8665241cd97746aff735ad86cc692c2f2a7af43895cc15e6e3f3d8b`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671546a39dce576ad9c3183ac8ec4dcbe1a6cb36f6c5b62c0493d409691ea5a`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:04a3896cf12d9c34ac580245d7479022e974248e7fc19c4738a299774f8ed323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137791397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094e8905c540f533e7ccd4b4714f49010f1dc5e8cd3da6a26c26e0afac51832`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:58:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:58:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:03:04 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:03:08 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:03:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:03:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:03:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:03:09 GMT
USER varnish
# Tue, 23 Jul 2024 02:03:09 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:03:10 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4f270ca2ccef2786b50cdffe74b172b9f27330341d9a33af90d3f0015ca88`  
		Last Modified: Tue, 23 Jul 2024 02:23:35 GMT  
		Size: 104.7 MB (104667110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea004555eaacc47df18a7b2c1fb069f096fc3912fc586d9686ed12162c5ba47`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d0aaf3a235a3b67bd395d526e0dab4d5c87bdac22b2038da3781d88fe2052`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; s390x

```console
$ docker pull varnish@sha256:6c70c3f4d8496e56f4871759210d0e2497beb8f5a4cbabe90790161b3b8188d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112436238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3497d261285d3c96c220d44a838a98350ba3af9c134494c618db7ebc3aa42c21`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:15:39 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 03:15:39 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 03:15:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 03:15:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 03:15:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:15:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:18:29 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 03:18:32 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:18:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:18:32 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 03:18:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:18:32 GMT
USER varnish
# Tue, 02 Jul 2024 03:18:32 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:18:33 GMT
CMD []
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b505a502c2de24553192f38047be900b2cf395ad6b5ca109aee88077abc5d9`  
		Last Modified: Tue, 02 Jul 2024 03:31:02 GMT  
		Size: 84.9 MB (84944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673e5987c1a2c4772ed24c9182a898ca45650d061f1f2cbd9195ae44aad87da`  
		Last Modified: Tue, 02 Jul 2024 03:30:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224c39e2e170d45f265be2f1715cc7ba3229e6810b60d96abc16078f0ae92532`  
		Last Modified: Tue, 02 Jul 2024 03:30:49 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5-alpine`

```console
$ docker pull varnish@sha256:d46a0dfaddfb1cf54972f5bd27fbba56393f1a26151f2f49dd13de9f1ab6292f
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
$ docker pull varnish@sha256:8424fb1713202c50485965f814bf58b94c65dc821c097ee57c64d7d6b8a6b87a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121b7a85a7a9aca89e33f5bbd22493e59e5df78827d63c1086bd888cc6e56a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 00:18:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:19:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 00:19:28 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:19:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:19:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:19:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:19:29 GMT
USER varnish
# Tue, 23 Jul 2024 00:19:29 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:19:29 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95974ecfc002b90880d3f022fe226ebe56dd0a09c3c39fff8099cf1d4210aa64`  
		Last Modified: Tue, 23 Jul 2024 00:25:08 GMT  
		Size: 69.8 MB (69794037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439adbfd9b4a8c49c54556a94474090aee3950956f11243597466161f099156b`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9109ac0fedbbf16db86f4a07d1f7c92b1c14c7d527de18b45994b72487ca298e`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8b0f6841e797901ccb26cd5c82a40f989fa82603dc18594b0861ac81f85715ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e282303d00881c4efb0c2cb0ecb2ab2b86cf92cd1eac2edcdb9e763d719f69a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:25:35 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:25:35 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:25:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:25:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:25:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:27:19 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:27:19 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:27:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:27:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:27:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:27:20 GMT
USER varnish
# Tue, 23 Jul 2024 01:27:20 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:27:20 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d03555dbfd17a222ed79e130c25aeb42730ad4541a60e400f65c83ad443c4e3`  
		Last Modified: Tue, 23 Jul 2024 01:33:27 GMT  
		Size: 54.5 MB (54491206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211bb2238f4f6c31dee263a42b48e6512bc5600993bc151da9e420ef4fbe5450`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297b5db4866df94ad4e2742793d5478485f31b57159208ae112dd3580cf4ff3`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8fb0864757c1b022eacb616f8788d9fc614b0e7860f7c0edbe39b474c981240d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450ea3ef23d2868ad41bd562624aad67398cc5dcb308ddab4274713b086b0364`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:36:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:37:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:37:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:37:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:37:07 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:37:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:37:08 GMT
USER varnish
# Tue, 23 Jul 2024 02:37:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:37:08 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e113b24d88cfa246b688fe1d04e1d651cacce4a48109704d9ef1b94895685398`  
		Last Modified: Tue, 23 Jul 2024 02:41:47 GMT  
		Size: 66.6 MB (66561723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b7ce770e5c43d7f09c101363d9ad5269a80f75479672baf5e371db55e5445`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761aab72ae34aa25910492d8150d95b6846a8e1fdf237d103c004315a74ca608`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:6c8ef34ac6de70f7d7e0b8b89ecd7da3d00790809c0a408b1cfb77f512c05b9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75240020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bdb26595488b3f0c2f5428728bf0979115141eedf12edd9039201d06c0f0f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:27:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:29:14 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:29:15 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:29:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:29:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:29:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:29:15 GMT
USER varnish
# Tue, 23 Jul 2024 02:29:15 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:29:16 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f74dc781e10d3e58c9c7cd87c8644641080aca4233b133b9b8e7dfec088189`  
		Last Modified: Tue, 23 Jul 2024 02:36:42 GMT  
		Size: 72.0 MB (71985396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df55ff2742c0663bac66792fd4fe4148d5e9c92b8e1ec8d57c931979f33486d9`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db91f66b153f4a88b55f0b698eea6ead55303511dae810272b7b47bf4656745`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c55791124a1fa4ced84f17e4e9daa5080c94a19af724ccd226945b888c695175
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70744493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72aaa8a85228492383959337ecbbdb7fddc68745076b201d9f3807f8acd00d4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:53:04 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 22 Jul 2024 23:53:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:54:24 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 22 Jul 2024 23:54:26 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:54:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:54:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:54:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:54:28 GMT
USER varnish
# Mon, 22 Jul 2024 23:54:28 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:54:28 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efc89745c19c2e51ab961c26ba90f1409971e9764c9854cc5cbc3181108579`  
		Last Modified: Tue, 23 Jul 2024 00:00:27 GMT  
		Size: 67.4 MB (67379364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8563234663e29a91149544caa9dc135919e628e2f729ed61100edb8fa2b51`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1178ac3f8574223e4b782d554ee328680e82722c0073805159070b7ff29db50d`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:87c20d607ac56f8ee7073b3d0a6817d552b250ae770da953f33937459f3f556f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65125894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b75d221855c4b5cea3718ab76ef08ff22a4b91312d776fd44bb83bfb2c337bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:06:38 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:07:58 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:08:00 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:08:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:08:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:08:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:08:00 GMT
USER varnish
# Tue, 23 Jul 2024 01:08:00 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:08:01 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a78f5ae1c60437eabf39f744119878113237b525886778a98274b64dfc211`  
		Last Modified: Tue, 23 Jul 2024 01:13:58 GMT  
		Size: 61.9 MB (61870800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a2daf5029c5109d48a91d6901ad71f9a8d77491622080cf761e0a8f330692`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a355efd0758b604c3dde42519ad784d41def0c5bbc034f6b4298e52809d29b5`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0`

```console
$ docker pull varnish@sha256:72bd165e75f85b8b73a619c70cd38ec9283abfe454b483ea51202e940ed2d084
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
$ docker pull varnish@sha256:c6245b1f63629f17d20d1d309de3f04aedf929e0a4281c8cd3a6a620daf384c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134862254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d25f7e828ba6e722bb372cb9999fd138682017e0d0b82b4b09a62257f6a9d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:53:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:56:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:56:01 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:56:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:56:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:56:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:56:01 GMT
USER varnish
# Tue, 02 Jul 2024 04:56:01 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:56:01 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16282c1add7c3baf6d62eb91f9434ef31e076bad8ac6529d2cbfd698fe683741`  
		Last Modified: Tue, 02 Jul 2024 05:08:45 GMT  
		Size: 105.7 MB (105733962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c568179d88274cbd7625ae74d29623d927c778a5f308ca67a42c6161e40344a1`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d438f5bf9894896e1ddf61c4267996ae7846e743e09b3ec47e2d3dc15054f33`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:65485dda4043010bd4ff6eb58d0b1701da60cfaedc861a70517d12eece89b467
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105116843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db62a170426bdff0051f3ec4d04b7c60e7333abe107705cfc17568b91dfa7f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:13:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:15:47 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:15:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:15:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:15:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:15:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:15:48 GMT
USER varnish
# Tue, 02 Jul 2024 04:15:48 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:15:48 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279719837527914fe9e5ff9709d81b1b0491eeed0cfb3c96ebf61511a68d10d8`  
		Last Modified: Tue, 02 Jul 2024 04:28:11 GMT  
		Size: 80.4 MB (80396664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72405d38d5b76fbbb94bd00812bb4bc48a94f476e840bdf82d60ff448ec3bafb`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3286e9b8ef98b08bbdee8bba6fca44840cf23c39848c227879d38b6f47a202c2`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:944e5e7eedff373706f516f36571fcc31e190d2b7e8693ad6528e62a23ee4b1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129339124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b778778b32af3328bcc517f80f8d47dfc7f858dedff1babf6ce45657180fa805`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:12:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:14:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:14:29 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:14:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:14:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:14:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:14:30 GMT
USER varnish
# Tue, 02 Jul 2024 04:14:30 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:14:30 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05fe21d9623c5387c391eec805dcd1526fb2ba19a3e0c4e632507c4f13e0dfd`  
		Last Modified: Tue, 02 Jul 2024 04:25:24 GMT  
		Size: 100.2 MB (100180549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d79257db29f3e1df4726e5423044d921f36494d042aca76d7b44cf787505`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3165c0b54f641e6fa1b49d6d5236759255cf0c4362f3df5b3219ffd917aa7be`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; 386

```console
$ docker pull varnish@sha256:bcaf2304278bbba8198a7fedb08acb5e6c43634378109924fccbd76a19a219f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132020835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24f1647d3dcad13568e201a9b3191c4aabe04495ecc18bada34219daac499b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 01:19:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:22:45 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:22:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:22:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:22:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:22:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:22:47 GMT
USER varnish
# Tue, 02 Jul 2024 01:22:47 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:22:48 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d32edbfc26351211befe908d30b1eada8a1223d9a90ebd1215a772c0861b2`  
		Last Modified: Tue, 02 Jul 2024 01:37:59 GMT  
		Size: 101.9 MB (101874548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdf815f8665241cd97746aff735ad86cc692c2f2a7af43895cc15e6e3f3d8b`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671546a39dce576ad9c3183ac8ec4dcbe1a6cb36f6c5b62c0493d409691ea5a`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:04a3896cf12d9c34ac580245d7479022e974248e7fc19c4738a299774f8ed323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137791397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094e8905c540f533e7ccd4b4714f49010f1dc5e8cd3da6a26c26e0afac51832`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:58:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:58:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:03:04 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:03:08 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:03:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:03:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:03:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:03:09 GMT
USER varnish
# Tue, 23 Jul 2024 02:03:09 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:03:10 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4f270ca2ccef2786b50cdffe74b172b9f27330341d9a33af90d3f0015ca88`  
		Last Modified: Tue, 23 Jul 2024 02:23:35 GMT  
		Size: 104.7 MB (104667110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea004555eaacc47df18a7b2c1fb069f096fc3912fc586d9686ed12162c5ba47`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d0aaf3a235a3b67bd395d526e0dab4d5c87bdac22b2038da3781d88fe2052`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; s390x

```console
$ docker pull varnish@sha256:a2ab708eed88d44d2e33921bc9673525c508f8baf93925ccba284e7c866eda01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112436029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729dc6a84568359196cc9893251e6d87091e64bc5771033db5ffbd598a7bc39`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 02:27:49 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Tue, 23 Jul 2024 02:27:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:25:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 03:25:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 03:25:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 03:25:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 03:25:18 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 03:27:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 03:27:45 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 03:27:45 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:27:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 03:27:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 03:27:45 GMT
USER varnish
# Tue, 23 Jul 2024 03:27:45 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 03:27:45 GMT
CMD []
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0f298f5ea636629583c7bb74172643b36a7b7fe33844a9645b1b77a757e043`  
		Last Modified: Tue, 23 Jul 2024 03:39:58 GMT  
		Size: 84.9 MB (84943920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b95bcd97f9daaacbef71368158b0a2e3fc01d08fcd8f042c8ad4852e27ddb`  
		Last Modified: Tue, 23 Jul 2024 03:39:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63979c06f1ee7ecc8e2b43664c3594622babd6fc5ae9247cb17e9baf5e45c801`  
		Last Modified: Tue, 23 Jul 2024 03:39:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0-alpine`

```console
$ docker pull varnish@sha256:d46a0dfaddfb1cf54972f5bd27fbba56393f1a26151f2f49dd13de9f1ab6292f
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
$ docker pull varnish@sha256:8424fb1713202c50485965f814bf58b94c65dc821c097ee57c64d7d6b8a6b87a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121b7a85a7a9aca89e33f5bbd22493e59e5df78827d63c1086bd888cc6e56a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 00:18:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:19:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 00:19:28 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:19:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:19:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:19:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:19:29 GMT
USER varnish
# Tue, 23 Jul 2024 00:19:29 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:19:29 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95974ecfc002b90880d3f022fe226ebe56dd0a09c3c39fff8099cf1d4210aa64`  
		Last Modified: Tue, 23 Jul 2024 00:25:08 GMT  
		Size: 69.8 MB (69794037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439adbfd9b4a8c49c54556a94474090aee3950956f11243597466161f099156b`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9109ac0fedbbf16db86f4a07d1f7c92b1c14c7d527de18b45994b72487ca298e`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8b0f6841e797901ccb26cd5c82a40f989fa82603dc18594b0861ac81f85715ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e282303d00881c4efb0c2cb0ecb2ab2b86cf92cd1eac2edcdb9e763d719f69a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:25:35 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:25:35 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:25:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:25:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:25:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:27:19 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:27:19 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:27:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:27:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:27:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:27:20 GMT
USER varnish
# Tue, 23 Jul 2024 01:27:20 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:27:20 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d03555dbfd17a222ed79e130c25aeb42730ad4541a60e400f65c83ad443c4e3`  
		Last Modified: Tue, 23 Jul 2024 01:33:27 GMT  
		Size: 54.5 MB (54491206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211bb2238f4f6c31dee263a42b48e6512bc5600993bc151da9e420ef4fbe5450`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297b5db4866df94ad4e2742793d5478485f31b57159208ae112dd3580cf4ff3`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8fb0864757c1b022eacb616f8788d9fc614b0e7860f7c0edbe39b474c981240d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450ea3ef23d2868ad41bd562624aad67398cc5dcb308ddab4274713b086b0364`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:36:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:37:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:37:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:37:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:37:07 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:37:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:37:08 GMT
USER varnish
# Tue, 23 Jul 2024 02:37:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:37:08 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e113b24d88cfa246b688fe1d04e1d651cacce4a48109704d9ef1b94895685398`  
		Last Modified: Tue, 23 Jul 2024 02:41:47 GMT  
		Size: 66.6 MB (66561723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b7ce770e5c43d7f09c101363d9ad5269a80f75479672baf5e371db55e5445`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761aab72ae34aa25910492d8150d95b6846a8e1fdf237d103c004315a74ca608`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:6c8ef34ac6de70f7d7e0b8b89ecd7da3d00790809c0a408b1cfb77f512c05b9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75240020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bdb26595488b3f0c2f5428728bf0979115141eedf12edd9039201d06c0f0f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:27:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:29:14 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:29:15 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:29:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:29:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:29:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:29:15 GMT
USER varnish
# Tue, 23 Jul 2024 02:29:15 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:29:16 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f74dc781e10d3e58c9c7cd87c8644641080aca4233b133b9b8e7dfec088189`  
		Last Modified: Tue, 23 Jul 2024 02:36:42 GMT  
		Size: 72.0 MB (71985396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df55ff2742c0663bac66792fd4fe4148d5e9c92b8e1ec8d57c931979f33486d9`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db91f66b153f4a88b55f0b698eea6ead55303511dae810272b7b47bf4656745`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c55791124a1fa4ced84f17e4e9daa5080c94a19af724ccd226945b888c695175
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70744493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72aaa8a85228492383959337ecbbdb7fddc68745076b201d9f3807f8acd00d4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:53:04 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 22 Jul 2024 23:53:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:54:24 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 22 Jul 2024 23:54:26 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:54:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:54:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:54:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:54:28 GMT
USER varnish
# Mon, 22 Jul 2024 23:54:28 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:54:28 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efc89745c19c2e51ab961c26ba90f1409971e9764c9854cc5cbc3181108579`  
		Last Modified: Tue, 23 Jul 2024 00:00:27 GMT  
		Size: 67.4 MB (67379364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8563234663e29a91149544caa9dc135919e628e2f729ed61100edb8fa2b51`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1178ac3f8574223e4b782d554ee328680e82722c0073805159070b7ff29db50d`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:87c20d607ac56f8ee7073b3d0a6817d552b250ae770da953f33937459f3f556f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65125894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b75d221855c4b5cea3718ab76ef08ff22a4b91312d776fd44bb83bfb2c337bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:06:38 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:07:58 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:08:00 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:08:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:08:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:08:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:08:00 GMT
USER varnish
# Tue, 23 Jul 2024 01:08:00 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:08:01 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a78f5ae1c60437eabf39f744119878113237b525886778a98274b64dfc211`  
		Last Modified: Tue, 23 Jul 2024 01:13:58 GMT  
		Size: 61.9 MB (61870800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a2daf5029c5109d48a91d6901ad71f9a8d77491622080cf761e0a8f330692`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a355efd0758b604c3dde42519ad784d41def0c5bbc034f6b4298e52809d29b5`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:d46a0dfaddfb1cf54972f5bd27fbba56393f1a26151f2f49dd13de9f1ab6292f
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
$ docker pull varnish@sha256:8424fb1713202c50485965f814bf58b94c65dc821c097ee57c64d7d6b8a6b87a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121b7a85a7a9aca89e33f5bbd22493e59e5df78827d63c1086bd888cc6e56a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 00:18:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:19:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 00:19:28 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:19:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:19:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:19:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:19:29 GMT
USER varnish
# Tue, 23 Jul 2024 00:19:29 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:19:29 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95974ecfc002b90880d3f022fe226ebe56dd0a09c3c39fff8099cf1d4210aa64`  
		Last Modified: Tue, 23 Jul 2024 00:25:08 GMT  
		Size: 69.8 MB (69794037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439adbfd9b4a8c49c54556a94474090aee3950956f11243597466161f099156b`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9109ac0fedbbf16db86f4a07d1f7c92b1c14c7d527de18b45994b72487ca298e`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8b0f6841e797901ccb26cd5c82a40f989fa82603dc18594b0861ac81f85715ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e282303d00881c4efb0c2cb0ecb2ab2b86cf92cd1eac2edcdb9e763d719f69a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:25:35 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:25:35 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:25:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:25:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:25:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:27:19 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:27:19 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:27:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:27:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:27:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:27:20 GMT
USER varnish
# Tue, 23 Jul 2024 01:27:20 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:27:20 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d03555dbfd17a222ed79e130c25aeb42730ad4541a60e400f65c83ad443c4e3`  
		Last Modified: Tue, 23 Jul 2024 01:33:27 GMT  
		Size: 54.5 MB (54491206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211bb2238f4f6c31dee263a42b48e6512bc5600993bc151da9e420ef4fbe5450`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297b5db4866df94ad4e2742793d5478485f31b57159208ae112dd3580cf4ff3`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8fb0864757c1b022eacb616f8788d9fc614b0e7860f7c0edbe39b474c981240d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450ea3ef23d2868ad41bd562624aad67398cc5dcb308ddab4274713b086b0364`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:36:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:37:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:37:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:37:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:37:07 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:37:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:37:08 GMT
USER varnish
# Tue, 23 Jul 2024 02:37:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:37:08 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e113b24d88cfa246b688fe1d04e1d651cacce4a48109704d9ef1b94895685398`  
		Last Modified: Tue, 23 Jul 2024 02:41:47 GMT  
		Size: 66.6 MB (66561723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b7ce770e5c43d7f09c101363d9ad5269a80f75479672baf5e371db55e5445`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761aab72ae34aa25910492d8150d95b6846a8e1fdf237d103c004315a74ca608`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:6c8ef34ac6de70f7d7e0b8b89ecd7da3d00790809c0a408b1cfb77f512c05b9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75240020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bdb26595488b3f0c2f5428728bf0979115141eedf12edd9039201d06c0f0f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:27:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:29:14 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:29:15 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:29:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:29:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:29:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:29:15 GMT
USER varnish
# Tue, 23 Jul 2024 02:29:15 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:29:16 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f74dc781e10d3e58c9c7cd87c8644641080aca4233b133b9b8e7dfec088189`  
		Last Modified: Tue, 23 Jul 2024 02:36:42 GMT  
		Size: 72.0 MB (71985396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df55ff2742c0663bac66792fd4fe4148d5e9c92b8e1ec8d57c931979f33486d9`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db91f66b153f4a88b55f0b698eea6ead55303511dae810272b7b47bf4656745`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c55791124a1fa4ced84f17e4e9daa5080c94a19af724ccd226945b888c695175
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70744493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72aaa8a85228492383959337ecbbdb7fddc68745076b201d9f3807f8acd00d4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:53:04 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 22 Jul 2024 23:53:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:54:24 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 22 Jul 2024 23:54:26 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:54:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:54:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:54:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:54:28 GMT
USER varnish
# Mon, 22 Jul 2024 23:54:28 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:54:28 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efc89745c19c2e51ab961c26ba90f1409971e9764c9854cc5cbc3181108579`  
		Last Modified: Tue, 23 Jul 2024 00:00:27 GMT  
		Size: 67.4 MB (67379364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8563234663e29a91149544caa9dc135919e628e2f729ed61100edb8fa2b51`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1178ac3f8574223e4b782d554ee328680e82722c0073805159070b7ff29db50d`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:87c20d607ac56f8ee7073b3d0a6817d552b250ae770da953f33937459f3f556f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65125894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b75d221855c4b5cea3718ab76ef08ff22a4b91312d776fd44bb83bfb2c337bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:06:38 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:07:58 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:08:00 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:08:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:08:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:08:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:08:00 GMT
USER varnish
# Tue, 23 Jul 2024 01:08:00 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:08:01 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a78f5ae1c60437eabf39f744119878113237b525886778a98274b64dfc211`  
		Last Modified: Tue, 23 Jul 2024 01:13:58 GMT  
		Size: 61.9 MB (61870800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a2daf5029c5109d48a91d6901ad71f9a8d77491622080cf761e0a8f330692`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a355efd0758b604c3dde42519ad784d41def0c5bbc034f6b4298e52809d29b5`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:72bd165e75f85b8b73a619c70cd38ec9283abfe454b483ea51202e940ed2d084
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
$ docker pull varnish@sha256:c6245b1f63629f17d20d1d309de3f04aedf929e0a4281c8cd3a6a620daf384c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134862254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d25f7e828ba6e722bb372cb9999fd138682017e0d0b82b4b09a62257f6a9d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:53:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:56:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:56:01 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:56:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:56:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:56:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:56:01 GMT
USER varnish
# Tue, 02 Jul 2024 04:56:01 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:56:01 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16282c1add7c3baf6d62eb91f9434ef31e076bad8ac6529d2cbfd698fe683741`  
		Last Modified: Tue, 02 Jul 2024 05:08:45 GMT  
		Size: 105.7 MB (105733962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c568179d88274cbd7625ae74d29623d927c778a5f308ca67a42c6161e40344a1`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d438f5bf9894896e1ddf61c4267996ae7846e743e09b3ec47e2d3dc15054f33`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:65485dda4043010bd4ff6eb58d0b1701da60cfaedc861a70517d12eece89b467
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105116843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db62a170426bdff0051f3ec4d04b7c60e7333abe107705cfc17568b91dfa7f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:13:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:15:47 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:15:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:15:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:15:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:15:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:15:48 GMT
USER varnish
# Tue, 02 Jul 2024 04:15:48 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:15:48 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279719837527914fe9e5ff9709d81b1b0491eeed0cfb3c96ebf61511a68d10d8`  
		Last Modified: Tue, 02 Jul 2024 04:28:11 GMT  
		Size: 80.4 MB (80396664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72405d38d5b76fbbb94bd00812bb4bc48a94f476e840bdf82d60ff448ec3bafb`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3286e9b8ef98b08bbdee8bba6fca44840cf23c39848c227879d38b6f47a202c2`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:944e5e7eedff373706f516f36571fcc31e190d2b7e8693ad6528e62a23ee4b1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129339124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b778778b32af3328bcc517f80f8d47dfc7f858dedff1babf6ce45657180fa805`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:12:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:14:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:14:29 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:14:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:14:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:14:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:14:30 GMT
USER varnish
# Tue, 02 Jul 2024 04:14:30 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:14:30 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05fe21d9623c5387c391eec805dcd1526fb2ba19a3e0c4e632507c4f13e0dfd`  
		Last Modified: Tue, 02 Jul 2024 04:25:24 GMT  
		Size: 100.2 MB (100180549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d79257db29f3e1df4726e5423044d921f36494d042aca76d7b44cf787505`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3165c0b54f641e6fa1b49d6d5236759255cf0c4362f3df5b3219ffd917aa7be`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:bcaf2304278bbba8198a7fedb08acb5e6c43634378109924fccbd76a19a219f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132020835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24f1647d3dcad13568e201a9b3191c4aabe04495ecc18bada34219daac499b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 01:19:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:22:45 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:22:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:22:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:22:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:22:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:22:47 GMT
USER varnish
# Tue, 02 Jul 2024 01:22:47 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:22:48 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d32edbfc26351211befe908d30b1eada8a1223d9a90ebd1215a772c0861b2`  
		Last Modified: Tue, 02 Jul 2024 01:37:59 GMT  
		Size: 101.9 MB (101874548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdf815f8665241cd97746aff735ad86cc692c2f2a7af43895cc15e6e3f3d8b`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671546a39dce576ad9c3183ac8ec4dcbe1a6cb36f6c5b62c0493d409691ea5a`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:04a3896cf12d9c34ac580245d7479022e974248e7fc19c4738a299774f8ed323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137791397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094e8905c540f533e7ccd4b4714f49010f1dc5e8cd3da6a26c26e0afac51832`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:58:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:58:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:03:04 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:03:08 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:03:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:03:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:03:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:03:09 GMT
USER varnish
# Tue, 23 Jul 2024 02:03:09 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:03:10 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4f270ca2ccef2786b50cdffe74b172b9f27330341d9a33af90d3f0015ca88`  
		Last Modified: Tue, 23 Jul 2024 02:23:35 GMT  
		Size: 104.7 MB (104667110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea004555eaacc47df18a7b2c1fb069f096fc3912fc586d9686ed12162c5ba47`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d0aaf3a235a3b67bd395d526e0dab4d5c87bdac22b2038da3781d88fe2052`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:a2ab708eed88d44d2e33921bc9673525c508f8baf93925ccba284e7c866eda01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112436029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729dc6a84568359196cc9893251e6d87091e64bc5771033db5ffbd598a7bc39`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 02:27:49 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Tue, 23 Jul 2024 02:27:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:25:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 03:25:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 03:25:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 03:25:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 03:25:18 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 03:27:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 03:27:45 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 03:27:45 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:27:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 03:27:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 03:27:45 GMT
USER varnish
# Tue, 23 Jul 2024 03:27:45 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 03:27:45 GMT
CMD []
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0f298f5ea636629583c7bb74172643b36a7b7fe33844a9645b1b77a757e043`  
		Last Modified: Tue, 23 Jul 2024 03:39:58 GMT  
		Size: 84.9 MB (84943920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b95bcd97f9daaacbef71368158b0a2e3fc01d08fcd8f042c8ad4852e27ddb`  
		Last Modified: Tue, 23 Jul 2024 03:39:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63979c06f1ee7ecc8e2b43664c3594622babd6fc5ae9247cb17e9baf5e45c801`  
		Last Modified: Tue, 23 Jul 2024 03:39:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:d46a0dfaddfb1cf54972f5bd27fbba56393f1a26151f2f49dd13de9f1ab6292f
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
$ docker pull varnish@sha256:8424fb1713202c50485965f814bf58b94c65dc821c097ee57c64d7d6b8a6b87a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121b7a85a7a9aca89e33f5bbd22493e59e5df78827d63c1086bd888cc6e56a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 00:18:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 00:18:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:18:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:19:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 00:19:28 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:19:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:19:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:19:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:19:29 GMT
USER varnish
# Tue, 23 Jul 2024 00:19:29 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:19:29 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95974ecfc002b90880d3f022fe226ebe56dd0a09c3c39fff8099cf1d4210aa64`  
		Last Modified: Tue, 23 Jul 2024 00:25:08 GMT  
		Size: 69.8 MB (69794037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439adbfd9b4a8c49c54556a94474090aee3950956f11243597466161f099156b`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9109ac0fedbbf16db86f4a07d1f7c92b1c14c7d527de18b45994b72487ca298e`  
		Last Modified: Tue, 23 Jul 2024 00:24:59 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8b0f6841e797901ccb26cd5c82a40f989fa82603dc18594b0861ac81f85715ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e282303d00881c4efb0c2cb0ecb2ab2b86cf92cd1eac2edcdb9e763d719f69a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:25:35 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:25:35 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:25:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:25:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:25:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:25:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:27:19 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:27:19 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:27:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:27:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:27:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:27:20 GMT
USER varnish
# Tue, 23 Jul 2024 01:27:20 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:27:20 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d03555dbfd17a222ed79e130c25aeb42730ad4541a60e400f65c83ad443c4e3`  
		Last Modified: Tue, 23 Jul 2024 01:33:27 GMT  
		Size: 54.5 MB (54491206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211bb2238f4f6c31dee263a42b48e6512bc5600993bc151da9e420ef4fbe5450`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297b5db4866df94ad4e2742793d5478485f31b57159208ae112dd3580cf4ff3`  
		Last Modified: Tue, 23 Jul 2024 01:33:20 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8fb0864757c1b022eacb616f8788d9fc614b0e7860f7c0edbe39b474c981240d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450ea3ef23d2868ad41bd562624aad67398cc5dcb308ddab4274713b086b0364`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:36:02 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:36:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:37:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:37:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:37:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:37:07 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:37:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:37:08 GMT
USER varnish
# Tue, 23 Jul 2024 02:37:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:37:08 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e113b24d88cfa246b688fe1d04e1d651cacce4a48109704d9ef1b94895685398`  
		Last Modified: Tue, 23 Jul 2024 02:41:47 GMT  
		Size: 66.6 MB (66561723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b7ce770e5c43d7f09c101363d9ad5269a80f75479672baf5e371db55e5445`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761aab72ae34aa25910492d8150d95b6846a8e1fdf237d103c004315a74ca608`  
		Last Modified: Tue, 23 Jul 2024 02:41:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:6c8ef34ac6de70f7d7e0b8b89ecd7da3d00790809c0a408b1cfb77f512c05b9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75240020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bdb26595488b3f0c2f5428728bf0979115141eedf12edd9039201d06c0f0f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 02:27:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 02:27:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:27:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:29:14 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:29:15 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:29:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:29:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:29:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:29:15 GMT
USER varnish
# Tue, 23 Jul 2024 02:29:15 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:29:16 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f74dc781e10d3e58c9c7cd87c8644641080aca4233b133b9b8e7dfec088189`  
		Last Modified: Tue, 23 Jul 2024 02:36:42 GMT  
		Size: 72.0 MB (71985396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df55ff2742c0663bac66792fd4fe4148d5e9c92b8e1ec8d57c931979f33486d9`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db91f66b153f4a88b55f0b698eea6ead55303511dae810272b7b47bf4656745`  
		Last Modified: Tue, 23 Jul 2024 02:36:30 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c55791124a1fa4ced84f17e4e9daa5080c94a19af724ccd226945b888c695175
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70744493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72aaa8a85228492383959337ecbbdb7fddc68745076b201d9f3807f8acd00d4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:53:04 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 22 Jul 2024 23:53:05 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 22 Jul 2024 23:53:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 22 Jul 2024 23:53:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:53:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:54:24 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 22 Jul 2024 23:54:26 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:54:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:54:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:54:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:54:28 GMT
USER varnish
# Mon, 22 Jul 2024 23:54:28 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:54:28 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efc89745c19c2e51ab961c26ba90f1409971e9764c9854cc5cbc3181108579`  
		Last Modified: Tue, 23 Jul 2024 00:00:27 GMT  
		Size: 67.4 MB (67379364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e8563234663e29a91149544caa9dc135919e628e2f729ed61100edb8fa2b51`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1178ac3f8574223e4b782d554ee328680e82722c0073805159070b7ff29db50d`  
		Last Modified: Tue, 23 Jul 2024 00:00:17 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:87c20d607ac56f8ee7073b3d0a6817d552b250ae770da953f33937459f3f556f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65125894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b75d221855c4b5cea3718ab76ef08ff22a4b91312d776fd44bb83bfb2c337bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:06:37 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:06:38 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:06:38 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:06:38 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:07:58 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 01:08:00 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:08:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:08:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:08:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:08:00 GMT
USER varnish
# Tue, 23 Jul 2024 01:08:00 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:08:01 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a78f5ae1c60437eabf39f744119878113237b525886778a98274b64dfc211`  
		Last Modified: Tue, 23 Jul 2024 01:13:58 GMT  
		Size: 61.9 MB (61870800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a2daf5029c5109d48a91d6901ad71f9a8d77491622080cf761e0a8f330692`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a355efd0758b604c3dde42519ad784d41def0c5bbc034f6b4298e52809d29b5`  
		Last Modified: Tue, 23 Jul 2024 01:13:51 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:5b95c1b1eef8cd37cc12767cbf42eef26961a3a3c1a436f5ff36603065baba2c
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
$ docker pull varnish@sha256:c6245b1f63629f17d20d1d309de3f04aedf929e0a4281c8cd3a6a620daf384c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134862254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d25f7e828ba6e722bb372cb9999fd138682017e0d0b82b4b09a62257f6a9d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:53:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:56:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:56:01 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:56:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:56:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:56:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:56:01 GMT
USER varnish
# Tue, 02 Jul 2024 04:56:01 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:56:01 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16282c1add7c3baf6d62eb91f9434ef31e076bad8ac6529d2cbfd698fe683741`  
		Last Modified: Tue, 02 Jul 2024 05:08:45 GMT  
		Size: 105.7 MB (105733962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c568179d88274cbd7625ae74d29623d927c778a5f308ca67a42c6161e40344a1`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d438f5bf9894896e1ddf61c4267996ae7846e743e09b3ec47e2d3dc15054f33`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:65485dda4043010bd4ff6eb58d0b1701da60cfaedc861a70517d12eece89b467
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105116843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db62a170426bdff0051f3ec4d04b7c60e7333abe107705cfc17568b91dfa7f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:13:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:13:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:13:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:15:47 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:15:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:15:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:15:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:15:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:15:48 GMT
USER varnish
# Tue, 02 Jul 2024 04:15:48 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:15:48 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279719837527914fe9e5ff9709d81b1b0491eeed0cfb3c96ebf61511a68d10d8`  
		Last Modified: Tue, 02 Jul 2024 04:28:11 GMT  
		Size: 80.4 MB (80396664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72405d38d5b76fbbb94bd00812bb4bc48a94f476e840bdf82d60ff448ec3bafb`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3286e9b8ef98b08bbdee8bba6fca44840cf23c39848c227879d38b6f47a202c2`  
		Last Modified: Tue, 02 Jul 2024 04:27:59 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:944e5e7eedff373706f516f36571fcc31e190d2b7e8693ad6528e62a23ee4b1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129339124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b778778b32af3328bcc517f80f8d47dfc7f858dedff1babf6ce45657180fa805`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:12:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:14:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:14:29 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:14:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:14:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:14:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:14:30 GMT
USER varnish
# Tue, 02 Jul 2024 04:14:30 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:14:30 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05fe21d9623c5387c391eec805dcd1526fb2ba19a3e0c4e632507c4f13e0dfd`  
		Last Modified: Tue, 02 Jul 2024 04:25:24 GMT  
		Size: 100.2 MB (100180549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d79257db29f3e1df4726e5423044d921f36494d042aca76d7b44cf787505`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3165c0b54f641e6fa1b49d6d5236759255cf0c4362f3df5b3219ffd917aa7be`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:bcaf2304278bbba8198a7fedb08acb5e6c43634378109924fccbd76a19a219f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132020835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24f1647d3dcad13568e201a9b3191c4aabe04495ecc18bada34219daac499b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 01:19:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 01:19:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 01:19:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:19:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:22:45 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:22:47 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:22:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:22:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:22:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:22:47 GMT
USER varnish
# Tue, 02 Jul 2024 01:22:47 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:22:48 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d32edbfc26351211befe908d30b1eada8a1223d9a90ebd1215a772c0861b2`  
		Last Modified: Tue, 02 Jul 2024 01:37:59 GMT  
		Size: 101.9 MB (101874548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdf815f8665241cd97746aff735ad86cc692c2f2a7af43895cc15e6e3f3d8b`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671546a39dce576ad9c3183ac8ec4dcbe1a6cb36f6c5b62c0493d409691ea5a`  
		Last Modified: Tue, 02 Jul 2024 01:37:39 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:04a3896cf12d9c34ac580245d7479022e974248e7fc19c4738a299774f8ed323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137791397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094e8905c540f533e7ccd4b4714f49010f1dc5e8cd3da6a26c26e0afac51832`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:58:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:58:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:03:04 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:03:08 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:03:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:03:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:03:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:03:09 GMT
USER varnish
# Tue, 23 Jul 2024 02:03:09 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:03:10 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4f270ca2ccef2786b50cdffe74b172b9f27330341d9a33af90d3f0015ca88`  
		Last Modified: Tue, 23 Jul 2024 02:23:35 GMT  
		Size: 104.7 MB (104667110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea004555eaacc47df18a7b2c1fb069f096fc3912fc586d9686ed12162c5ba47`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d0aaf3a235a3b67bd395d526e0dab4d5c87bdac22b2038da3781d88fe2052`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:6c70c3f4d8496e56f4871759210d0e2497beb8f5a4cbabe90790161b3b8188d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112436238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3497d261285d3c96c220d44a838a98350ba3af9c134494c618db7ebc3aa42c21`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:15:39 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 03:15:39 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 03:15:39 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 03:15:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 03:15:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 03:15:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:15:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:18:29 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 03:18:32 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:18:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:18:32 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 03:18:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:18:32 GMT
USER varnish
# Tue, 02 Jul 2024 03:18:32 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:18:33 GMT
CMD []
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b505a502c2de24553192f38047be900b2cf395ad6b5ca109aee88077abc5d9`  
		Last Modified: Tue, 02 Jul 2024 03:31:02 GMT  
		Size: 84.9 MB (84944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673e5987c1a2c4772ed24c9182a898ca45650d061f1f2cbd9195ae44aad87da`  
		Last Modified: Tue, 02 Jul 2024 03:30:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224c39e2e170d45f265be2f1715cc7ba3229e6810b60d96abc16078f0ae92532`  
		Last Modified: Tue, 02 Jul 2024 03:30:49 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:5d530300a67f49028a8c18f6594c0df7ae4ba8cc75f9e207dca1b7c716e14b93
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
$ docker pull varnish@sha256:37d1ea00fcf52fdfb5b228053837545340672854a4b7dd4606d9d96adc5ca12e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134753494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7d06ba279ae2c10547844ab1808d6a20433302743582cf112afce5a4f1bedd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:56:07 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:56:07 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:56:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:56:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:56:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:56:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:58:40 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:58:41 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:58:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:58:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:58:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:58:42 GMT
USER varnish
# Tue, 02 Jul 2024 04:58:42 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566c8207791dedf3cf2fabd31800137df06433f4cba49cbb4ed9347b7e968016`  
		Last Modified: Tue, 02 Jul 2024 05:09:12 GMT  
		Size: 105.6 MB (105625204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42777929956d21d20e906e63c3ba3cd63456bd6bbb8f22bc0872ce9d1751eae1`  
		Last Modified: Tue, 02 Jul 2024 05:08:58 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6f80adf2bdd552cecb9f53beb70f3f5d7fc40005a3e6d401872f0e663294`  
		Last Modified: Tue, 02 Jul 2024 05:08:58 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:da0f5f1f8d0780b6bdc532f6eb5f5e19bade34a56388d538123a40233981021b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105006912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c825ef849dcdf5eb5b8e600e94e950b7370bc2f2871ba65768602c0c95d5745`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:13:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:15:57 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:15:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:15:58 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:15:58 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:15:58 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:15:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:18:22 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:18:23 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:18:23 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:18:23 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:18:24 GMT
USER varnish
# Tue, 02 Jul 2024 04:18:24 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:18:24 GMT
CMD []
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e593b868ecc81ea854f53f4203520e212ec48e0ebc0a66a3b038442888dd855d`  
		Last Modified: Tue, 02 Jul 2024 04:28:37 GMT  
		Size: 80.3 MB (80286730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a775be51a6ee113268f6cafefb62c1fb81d5c7b9dcb4ee50d01cd16faa6c5d`  
		Last Modified: Tue, 02 Jul 2024 04:28:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a8d356d15205b57b447d216aca09fc08292c11f03463fd15db5938abedc0b`  
		Last Modified: Tue, 02 Jul 2024 04:28:25 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a501bc6a04026e50e398c964eeeb51b23516235bf1a364b4f64278a6bbc9e99b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129240869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d99c669f1ceed553ea0eeb32605f54a52c544620b53c55cfd2d0e4f801d2fd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 04:14:46 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 04:14:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 04:14:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:14:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:14:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:16:58 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:17:00 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:17:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:17:00 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:17:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:17:00 GMT
USER varnish
# Tue, 02 Jul 2024 04:17:00 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:17:00 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8bc01a8a92806672a3bfb149055600e15dc2ebba3247d37c6c11ed4c8cdad`  
		Last Modified: Tue, 02 Jul 2024 04:25:48 GMT  
		Size: 100.1 MB (100082293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3db704216eba227d8273c192ec346e358193854ae6ac4c3ba416b573c2d190`  
		Last Modified: Tue, 02 Jul 2024 04:25:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4b69b5d1eaeadd1cfacffbc26e1e64d2934bfa22754cb5f9dd31d87d9de9d8`  
		Last Modified: Tue, 02 Jul 2024 04:25:36 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:cfb7e07dbe578ce715c8397200534fdebd68d60368ab76c2090ca05e261cc639
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131926704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a36699d08e55346abcda2529970f40066c0f1093e983f5b9b816b8dc8545d00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 01:22:54 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 01:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 01:22:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 01:22:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 01:22:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:26:08 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 01:26:10 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:26:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:26:10 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 01:26:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:26:11 GMT
USER varnish
# Tue, 02 Jul 2024 01:26:11 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:26:11 GMT
CMD []
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022680d52f70894469d7c28d759fcb6cc1af7ddb0e1eb97ceeac9c4242b9b3fe`  
		Last Modified: Tue, 02 Jul 2024 01:38:31 GMT  
		Size: 101.8 MB (101780415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8641c300252521fa15bfb445ed8134c6bf7b6a5c99e481d656fbc3b9707b28`  
		Last Modified: Tue, 02 Jul 2024 01:38:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf14b6ded3b7274948e430a9c35ca995e6d2cd0154738ee27a50002b37a9870`  
		Last Modified: Tue, 02 Jul 2024 01:38:11 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:1def881556ab48080e777d8f6d22ec19ada032a5dba828b2e71ef7a4a35d6cba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137693599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b0ecf3467a4156469bfbe6cdd1a525727f67197b668e92e1d91a7bd814b23d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:03:25 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:03:25 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:03:26 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:03:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:03:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:03:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 02:03:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:07:30 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:07:34 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:07:34 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:07:35 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:07:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:07:36 GMT
USER varnish
# Tue, 23 Jul 2024 02:07:36 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:07:36 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7a2c43b896069ccdf5ea950ed605b4a0b958b8faa94693fd918248ded3d47f`  
		Last Modified: Tue, 23 Jul 2024 02:24:04 GMT  
		Size: 104.6 MB (104569312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2846c911c8a8733da1790dbc02bb73238b1616c8613df2bf297469ff2f05ad`  
		Last Modified: Tue, 23 Jul 2024 02:23:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805c71dead9d8bfb40fe7c28613a776ad2fe4ff1be6cc73b26964efcf7b9006d`  
		Last Modified: Tue, 23 Jul 2024 02:23:47 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:548459afd525a54eb52e7e894a1b0fe1b53ce0ea30b41df24454b6d125f7f87d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112340105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078de114c46737c3e9118e346a9f2586976adc8f417687f251b9aeecef31a57`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:15:39 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 03:18:54 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 02 Jul 2024 03:18:54 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 02 Jul 2024 03:18:54 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 02 Jul 2024 03:18:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 02 Jul 2024 03:18:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 03:18:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 03:18:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:21:09 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 03:21:12 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:21:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:21:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 03:21:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:21:12 GMT
USER varnish
# Tue, 02 Jul 2024 03:21:12 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:21:13 GMT
CMD []
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc3c811cb63b01096d259387bd31a4ceaaa31de3560294006525cd38de3a9dd`  
		Last Modified: Tue, 02 Jul 2024 03:31:22 GMT  
		Size: 84.8 MB (84848004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa4ddfaa7c86e7691b9de08dd07300c2163874027a9df0dd78a6a0d12f1485`  
		Last Modified: Tue, 02 Jul 2024 03:31:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e15199fe8065c4a7ec6991a0150e8988673234bd59b0a3618ad93b8f25e203c`  
		Last Modified: Tue, 02 Jul 2024 03:31:10 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:704092e07547d966900898f7d71e3fc1e11cf062cdaff09659b92ec5677fccf8
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
$ docker pull varnish@sha256:627cff1fdecac0904f7d6f767ade41ed354697530014be0c02aa28ded143af7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2298b48360e011b725d026b4a28a533c54c78b5046af35617dd90790c0116ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:18:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 00:19:39 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 00:19:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 00:19:40 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 00:19:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 00:19:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 00:19:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 00:19:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 00:21:02 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 00:21:02 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 00:21:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:21:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 00:21:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 00:21:03 GMT
USER varnish
# Tue, 23 Jul 2024 00:21:03 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 00:21:03 GMT
CMD []
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62d6dfb9e82e0a7c05c07cb2ddbb6063b9e223093be1be57f917f648c389df5`  
		Last Modified: Tue, 23 Jul 2024 00:25:29 GMT  
		Size: 69.7 MB (69703561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108ea953524427a74b8e4003df1d92066bb9b65a7689df697de4e034192fcf3`  
		Last Modified: Tue, 23 Jul 2024 00:25:20 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d819bb73a613ed5355434fdf1b76ea822d24a868b54af7cb7eb914c2f5201cea`  
		Last Modified: Tue, 23 Jul 2024 00:25:20 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3c26c259ff513521c809b737cf7c4db2f45e0fcb2fe5982b89e4e53d95d3239b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57327047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab3561e54c063f20cf3e0ac756eaf3a39d6ce572a2866b3b2c23c50e40b12e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:25:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 01:27:30 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:27:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:27:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:27:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:27:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:27:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:29:07 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:29:07 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:29:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:29:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:29:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:29:08 GMT
USER varnish
# Tue, 23 Jul 2024 01:29:08 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:29:08 GMT
CMD []
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffefcdaabd64405cde52b5bfc485da2f6f6b676c13cb39b8f6522fc9d1594a19`  
		Last Modified: Tue, 23 Jul 2024 01:33:44 GMT  
		Size: 54.4 MB (54397919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb267507ecb05fc645190517c37cd1b296f9af2e118c8439d2b14c5d965a07d`  
		Last Modified: Tue, 23 Jul 2024 01:33:38 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0888f8ed2e6566df6eb66c3ee86b80ca98f5a24ebf7d0fa61542db60a9612c8e`  
		Last Modified: Tue, 23 Jul 2024 01:33:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:323ff4d1330b61943f18d1d0ff9794ad7acf045e943c539fc1249bf1211a5cbc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69826933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ed7787250fde0fffc58cfc97de470ee64b113d554003c768f086e70eeae4f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:36:02 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:37:13 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:37:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:37:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:37:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:37:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:38:23 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:38:24 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:38:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:38:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:38:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:38:24 GMT
USER varnish
# Tue, 23 Jul 2024 02:38:24 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:38:24 GMT
CMD []
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c75650c9e9beb0a0b55b6521bf2c00e229b25ce1da391bc2b51c20034f7715`  
		Last Modified: Tue, 23 Jul 2024 02:42:05 GMT  
		Size: 66.5 MB (66466452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782e41c252bdd7b99370d9bceb9a0a4e626667831c25eedb78975fbcd9812466`  
		Last Modified: Tue, 23 Jul 2024 02:41:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caf1aa65ec481deb40e5763e6b430a369311339764cddce0cea51b02ac40137`  
		Last Modified: Tue, 23 Jul 2024 02:42:00 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:93d18ad0c95d0deb3c906a588cf6d311db49951f2fdb9abb68da62fac415ac57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75146245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6926482de52318c54726ad8e2fa23c44786aab22c8e75184a9a17dcc84033e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:27:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 02:29:31 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 02:29:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 02:29:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 02:29:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 02:29:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:31:30 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 02:31:31 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:31:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:31:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:31:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:31:31 GMT
USER varnish
# Tue, 23 Jul 2024 02:31:31 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:31:31 GMT
CMD []
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1b4cbd7f1a5cf901465ed58deb6357f76f9211644022ce88c5d5920d6d167a`  
		Last Modified: Tue, 23 Jul 2024 02:37:05 GMT  
		Size: 71.9 MB (71891627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a34a55e7f14e39e8e2cbda4ef23cf40ed97fb7a1d7167cec8d6b89300806a3`  
		Last Modified: Tue, 23 Jul 2024 02:36:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ffec8c83931eceb1a10310c300cf14063872ece7746b7627ec425ce98b8cc6`  
		Last Modified: Tue, 23 Jul 2024 02:36:53 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:ccd5208b46c61c09985bf6a62cfc23e359dc4a735ca89e66eb6d75edd99be95a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70649093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7db6c58c9661a31f4581894a4ed80f1cd031b1ad69a58b3c55d3a93677e776`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:53:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 22 Jul 2024 23:54:46 GMT
ARG VARNISH_VERSION=7.4.3
# Mon, 22 Jul 2024 23:54:46 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Mon, 22 Jul 2024 23:54:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 22 Jul 2024 23:54:47 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Mon, 22 Jul 2024 23:54:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Mon, 22 Jul 2024 23:54:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 22 Jul 2024 23:54:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jul 2024 23:54:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jul 2024 23:56:06 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Mon, 22 Jul 2024 23:56:08 GMT
WORKDIR /etc/varnish
# Mon, 22 Jul 2024 23:56:09 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 22 Jul 2024 23:56:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 22 Jul 2024 23:56:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jul 2024 23:56:10 GMT
USER varnish
# Mon, 22 Jul 2024 23:56:10 GMT
EXPOSE 80 8443
# Mon, 22 Jul 2024 23:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c497a12642e96290baee7f966db9cb2744473cf6812498312cd099d9e4c788`  
		Last Modified: Tue, 23 Jul 2024 00:00:48 GMT  
		Size: 67.3 MB (67283965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faad1c1f35306fb4d2e94bd212b097e210af7aa489f14f474981e4bd0966f8eb`  
		Last Modified: Tue, 23 Jul 2024 00:00:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e80c54b9ae6306112403d683f5c81013cccd2f3d65c26bdde78a3f274b16f6`  
		Last Modified: Tue, 23 Jul 2024 00:00:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:26e24c18193128808a01eb0041756acf7a3993a707f2ae9a834b39c730552a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65025041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290c0fef2dba059a5b8af56803d0a87ebad56ad7fe4f62f4a1860e357865ce0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:06:37 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 23 Jul 2024 01:08:20 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:08:20 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 23 Jul 2024 01:08:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 23 Jul 2024 01:08:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:08:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 23 Jul 2024 01:08:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 01:09:45 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 23 Jul 2024 01:09:47 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 01:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:09:47 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 01:09:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 01:09:48 GMT
USER varnish
# Tue, 23 Jul 2024 01:09:48 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 01:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e066951adfe18da6dc61367ee5810bf1308f7cb284457d8b0f0bb7fb5213cbd`  
		Last Modified: Tue, 23 Jul 2024 01:14:15 GMT  
		Size: 61.8 MB (61769943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc0b53e844c962ccc1922fb4fa3f8d4cf4c33abae2d8262e874e26d62c77cbd`  
		Last Modified: Tue, 23 Jul 2024 01:14:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010fd03a1011d817ebf0b5574407ede3696fcf1623c3422b76eac7d0e48844c7`  
		Last Modified: Tue, 23 Jul 2024 01:14:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:fae44b93f72c103a1b07ef5046d3969ef43d6abed9d0637c6defee605d6c1aa5
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
$ docker pull varnish@sha256:5360318539dc8b05fed21a56d06012897d8af9c24b26bcafb0b5308afbf1fb9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95861714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5385e986c1d5875ef038b503478bf76b2fc9f20f7cdbe33f1903c9305f4e926`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:58:49 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:58:49 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:58:49 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:58:49 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 05:00:41 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 05:00:42 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 05:00:42 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:00:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 05:00:42 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 05:00:42 GMT
CMD []
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4769cf1c2ed5001dd80925ff94b3ec6e9ec0590f9616de69fee984cb032b958`  
		Last Modified: Tue, 02 Jul 2024 05:09:32 GMT  
		Size: 64.4 MB (64438714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fc65480a218650c313c4a173739cc2cc2e0d6c6afe08e9f19d3dee30174724`  
		Last Modified: Tue, 02 Jul 2024 05:09:23 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:486b9ce4259d2561cbb8351e9399b0e7a37d46a5b54686ee171db952b6340a95
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72858021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0068cb3ef05f75aff684597cef85b1ec67250cdbc036a34a3334eaf33d4edaf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:18:37 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:18:37 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:18:37 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:18:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:20:17 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:20:17 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:20:18 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:20:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:20:18 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:20:18 GMT
CMD []
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13aaf79ba297cbd68c00cf789f9ea5b12a54286f7866d0da0b9a2a59da5562`  
		Last Modified: Tue, 02 Jul 2024 04:28:54 GMT  
		Size: 46.3 MB (46274599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5d92f8b4f09f971eaade8d1c87937f7806fdb4e56674d1128ac335d6b702be`  
		Last Modified: Tue, 02 Jul 2024 04:28:48 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:bd45ac8e31ba63a70c63cf2a4265796b8d305d8404e98cdbe6b2ed1a599fa165
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89958871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad02409b9bf71292b1cea6c39522bb99d628f3f3599e9297809586c6f1bc2ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:17:10 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 04:17:10 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 04:17:10 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 04:17:10 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:18:37 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 04:18:38 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:18:38 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:18:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:18:38 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:18:38 GMT
CMD []
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153d5c1d94c4804c2f448d050f817e1b3a110b3691de7cfb3783dff8879b6071`  
		Last Modified: Tue, 02 Jul 2024 04:26:05 GMT  
		Size: 59.9 MB (59888542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9376107d7d3e15b00fa56b3254347d2a47b17033daf68faa87e04a8ffb4df72b`  
		Last Modified: Tue, 02 Jul 2024 04:25:58 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:f1dc85300798a3e31f0c1b60936cd276cd10fe553296882d451213d5fc6399d8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97129607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f53ffb2d85e94505ed523fa67cc60f4ed3a62eec09e4526fa7167d51650a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:18 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 01:26:19 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 01:26:19 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 01:26:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 01:28:31 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 01:28:32 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 01:28:32 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:28:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 01:28:32 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 01:28:33 GMT
CMD []
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa8474d680a30423f88095d021431e2a707a59c23532c6c3c33bfc2e6a407c`  
		Last Modified: Tue, 02 Jul 2024 01:38:53 GMT  
		Size: 64.7 MB (64720438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b6d78caf142afa6cbc9dbed69d2647deb8f6f6dd544fda612138aef734af0`  
		Last Modified: Tue, 02 Jul 2024 01:38:41 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:c74197383e5c1f4b20ae2339761ca885a98b272697c13be553456aaf81dadad7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94652569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91f64258a18157b0d658c98a06d27accdaf80f15e638c7793992363cdcaade8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:07:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 23 Jul 2024 02:07:54 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 23 Jul 2024 02:07:54 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 23 Jul 2024 02:07:55 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:11:09 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 02:11:12 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:11:12 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:11:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:11:13 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:11:14 GMT
CMD []
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22da0b5a4215694a5c74a41f0204a084ef5fbbbfcf338b0415ac36afe9623b0d`  
		Last Modified: Tue, 23 Jul 2024 02:24:24 GMT  
		Size: 59.3 MB (59346651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93a758e1759711d142c2eb2130e6323ef163a6c103b397fdccd3da8c01b16d`  
		Last Modified: Tue, 23 Jul 2024 02:24:14 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:94b3253a58f856134ae2d7d5aae089fdf6bc02565013c66ea9939499ed87a6d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fad799339b5dd8c54c2033c029e361a51f86ed2b63c01777d15ddab2fff735e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:21:39 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 02 Jul 2024 03:21:39 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 02 Jul 2024 03:21:39 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 02 Jul 2024 03:21:39 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 03:23:30 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Jul 2024 03:23:31 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 03:23:31 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:23:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 03:23:31 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 03:23:32 GMT
CMD []
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5719f582c9346191e5e2cc39cb6fd6647b2ff915cbcd2c11d34b6ddb7d43d019`  
		Last Modified: Tue, 02 Jul 2024 03:31:36 GMT  
		Size: 46.6 MB (46595231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c364ebc518cea7f92cc62c044945fa809d7deb10db3e7c59fdd793a80d20d73d`  
		Last Modified: Tue, 02 Jul 2024 03:31:29 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
