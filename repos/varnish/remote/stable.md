## `varnish:stable`

```console
$ docker pull varnish@sha256:eb35078c3b108978b2815b6f1d91317584fcddf602b74eb2aeb3cfc084aa369d
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
$ docker pull varnish@sha256:dd2657d4f6228f4547ff50a022390eb04f0153a43b585d6248d05d1016eb941c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72864171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6eefd167a7307bad3930f642334432543b88f8443abab53d79026180293c7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:03:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 23 Jul 2024 04:03:42 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 23 Jul 2024 04:03:43 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 23 Jul 2024 04:03:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 04:06:38 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 04:06:39 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 04:06:39 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:06:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 04:06:40 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 04:06:40 GMT
CMD []
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87960271eaa43570616c93fe0a509827e124a891df03cdb5f0de74be1dc0dbc0`  
		Last Modified: Tue, 23 Jul 2024 04:20:02 GMT  
		Size: 46.3 MB (46274322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe53fbcdb1e5a4309b076bfd4859a94258cdb732f63c84f8fbd7c63553a67b3`  
		Last Modified: Tue, 23 Jul 2024 04:19:53 GMT  
		Size: 719.0 B  
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
$ docker pull varnish@sha256:e12875ee828d7f308c82af1bb912c1233b9b39184348ae8ee0d181aa135bbb9c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97131699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea671c08969eb62d178f0dc5765b16f138acd9f1f2c8582c653ef7c5463b392e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 03:54:35 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Tue, 23 Jul 2024 03:54:36 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:24:46 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 23 Jul 2024 04:24:46 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 23 Jul 2024 04:24:46 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 23 Jul 2024 04:24:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 04:26:56 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 04:26:56 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 04:26:57 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:26:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 04:26:57 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 04:26:57 GMT
CMD []
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a987a0e08f46a39fdcac1685a6fab366de99315e630f5affb41c3edb15df40db`  
		Last Modified: Tue, 23 Jul 2024 04:37:20 GMT  
		Size: 64.7 MB (64717175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef86f26aa79c702efa962d181290d4205fab65688319230326dc6e544e0f63ce`  
		Last Modified: Tue, 23 Jul 2024 04:37:08 GMT  
		Size: 716.0 B  
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
$ docker pull varnish@sha256:4048d48f532f935870471bf544b9950285bb57adc2015d944b36f7b0c8b99827
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76264582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09174ceb4447657594c4f581bc0917283ba92b86421c79d03528e215d4f7c10a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 02:28:25 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Tue, 23 Jul 2024 02:28:26 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:30:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 23 Jul 2024 03:30:48 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 23 Jul 2024 03:30:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 23 Jul 2024 03:30:48 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 03:32:18 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 23 Jul 2024 03:32:20 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 03:32:20 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:32:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 03:32:20 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 03:32:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f428f6eee1f80cae007c90f292d38351051d2d558cd3e38cb11007cff6355db4`  
		Last Modified: Tue, 23 Jul 2024 03:40:33 GMT  
		Size: 46.6 MB (46594845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d021d5c93decfee67ad5e0184bf2535ea9cd4609d1f3abd62751147f881c4b44`  
		Last Modified: Tue, 23 Jul 2024 03:40:27 GMT  
		Size: 719.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
