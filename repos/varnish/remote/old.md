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
