## `varnish:latest`

```console
$ docker pull varnish@sha256:769ac3c32ad36169a1c0282382a57cdb1ddd8064706ed5b3cad2d004a8bbbb40
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
$ docker pull varnish@sha256:03e7484f1a2bd7050872ffb88f835d8b8d314cd9243669374ecedd3468202649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134732997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d926e8ce30512eaab9d4a8fd28fe009d7f3c1c148dce61a86058f14ae5387b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 08:01:04 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 13 Feb 2024 08:01:04 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 13 Feb 2024 08:01:05 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 13 Feb 2024 08:01:05 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 13 Feb 2024 08:01:05 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 13 Feb 2024 08:01:05 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 13 Feb 2024 08:01:05 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 13 Feb 2024 08:01:05 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 13 Feb 2024 08:01:05 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 13 Feb 2024 08:01:05 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 Feb 2024 08:01:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Feb 2024 08:03:48 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Feb 2024 08:03:49 GMT
WORKDIR /etc/varnish
# Tue, 13 Feb 2024 08:03:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:03:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Feb 2024 08:03:49 GMT
USER varnish
# Tue, 13 Feb 2024 08:03:49 GMT
EXPOSE 80 8443
# Tue, 13 Feb 2024 08:03:50 GMT
CMD []
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd88fa63ef8529e5dbdfebcc12878262c09cbf248f192cae9662f843e3e5361`  
		Last Modified: Tue, 13 Feb 2024 08:09:00 GMT  
		Size: 105.6 MB (105608417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c91a152808060474c4931fddbb0fc2840406d44c4000a40d502eb776a95a92`  
		Last Modified: Tue, 13 Feb 2024 08:08:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:61d30454cc58f79771dad0816f9f01e93ff3ddfc5d884a76e3646168db176457
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104968912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b883be56dcf8cfa22b7cccd1cb2be2e1a6ad1a3b7f2fe59c26c3b13f2c0d25`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:33:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 13 Feb 2024 04:33:55 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 13 Feb 2024 04:33:55 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 13 Feb 2024 04:33:56 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 13 Feb 2024 04:33:56 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 13 Feb 2024 04:33:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 13 Feb 2024 04:33:56 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 13 Feb 2024 04:33:57 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 13 Feb 2024 04:33:57 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 13 Feb 2024 04:33:57 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 Feb 2024 04:33:57 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Feb 2024 04:42:10 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Feb 2024 04:42:11 GMT
WORKDIR /etc/varnish
# Tue, 13 Feb 2024 04:42:11 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 13 Feb 2024 04:42:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Feb 2024 04:42:12 GMT
USER varnish
# Tue, 13 Feb 2024 04:42:12 GMT
EXPOSE 80 8443
# Tue, 13 Feb 2024 04:42:13 GMT
CMD []
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27092bc1f350004e36a95a7810c65d13402c5848cb3662e03d51e8bc75d4126e`  
		Last Modified: Tue, 13 Feb 2024 04:50:33 GMT  
		Size: 80.3 MB (80251776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b867965ec61f1763017a808c58b27bc169852aab0de753ce163b665f35d5d`  
		Last Modified: Tue, 13 Feb 2024 04:50:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:86fdc5b39084974a03e92119c2cbf1ec01716049fd25b547d27f7e3fd6f05928
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129218701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800fd6cec6592f69f8a2279a1adee13e5dc90559fbc3ad0fdceb314da4faaf97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:25:07 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 13 Feb 2024 07:25:07 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 13 Feb 2024 07:25:07 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 13 Feb 2024 07:25:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 13 Feb 2024 07:25:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 13 Feb 2024 07:25:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 13 Feb 2024 07:25:07 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 13 Feb 2024 07:25:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 13 Feb 2024 07:25:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 13 Feb 2024 07:25:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 Feb 2024 07:25:08 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Feb 2024 07:27:32 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Feb 2024 07:27:33 GMT
WORKDIR /etc/varnish
# Tue, 13 Feb 2024 07:27:34 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 13 Feb 2024 07:27:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Feb 2024 07:27:34 GMT
USER varnish
# Tue, 13 Feb 2024 07:27:34 GMT
EXPOSE 80 8443
# Tue, 13 Feb 2024 07:27:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417a1b31a391b7afd1355af16946eabdd40734d25be8c3edf97d8dfed5c2bab0`  
		Last Modified: Tue, 13 Feb 2024 07:32:12 GMT  
		Size: 100.1 MB (100061848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c46e5a3655ce1948f427d79227bab862d8c2eab9d1f365b8206b2c70d168f1c`  
		Last Modified: Tue, 13 Feb 2024 07:32:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:71dcd8a74429290e3682727a98a0122adae6648b193a95b58bd9085d01299cb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131940164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7fc89f0113f18741b15d9c951d9c6e995ac754a79a4520f8f2553e5a6da14`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Jan 2024 22:39:00 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 31 Jan 2024 22:39:01 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 11:13:00 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 01 Feb 2024 11:13:01 GMT
ARG VARNISH_VERSION=7.4.2
# Thu, 01 Feb 2024 11:13:01 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Thu, 01 Feb 2024 11:13:01 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 01 Feb 2024 11:13:01 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 01 Feb 2024 11:13:01 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 01 Feb 2024 11:13:01 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Thu, 01 Feb 2024 11:13:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Thu, 01 Feb 2024 11:13:02 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Thu, 01 Feb 2024 11:13:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 01 Feb 2024 11:13:02 GMT
ENV VARNISH_SIZE=100M
# Thu, 01 Feb 2024 11:16:41 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 01 Feb 2024 11:16:43 GMT
WORKDIR /etc/varnish
# Thu, 01 Feb 2024 11:16:43 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 01 Feb 2024 11:16:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 01 Feb 2024 11:16:43 GMT
USER varnish
# Thu, 01 Feb 2024 11:16:43 GMT
EXPOSE 80 8443
# Thu, 01 Feb 2024 11:16:43 GMT
CMD []
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f15ed5d87a7d2cc0ae08c489c5b886e9431392f5ac256b3a4b1e0b7e2bccf2`  
		Last Modified: Thu, 01 Feb 2024 11:23:19 GMT  
		Size: 101.8 MB (101774653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4e114247b551f1cafd655f58cbba19cc4b158b84ba84992e6bbd0408fb9271`  
		Last Modified: Thu, 01 Feb 2024 11:22:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:01e4a112888fed0943ddb09e7aff5d359715b40310ce21bc8e3c41f020423538
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137654959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fc818aea3831693321e91622840c7a29e927ed98b40ce469bcea51d7dff404`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 06:59:08 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 13 Feb 2024 06:59:09 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 13 Feb 2024 06:59:09 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 13 Feb 2024 06:59:10 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 13 Feb 2024 06:59:11 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 13 Feb 2024 06:59:11 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 13 Feb 2024 06:59:12 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 13 Feb 2024 06:59:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 13 Feb 2024 06:59:13 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 13 Feb 2024 06:59:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 Feb 2024 06:59:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Feb 2024 07:05:34 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Feb 2024 07:05:39 GMT
WORKDIR /etc/varnish
# Tue, 13 Feb 2024 07:05:39 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 13 Feb 2024 07:05:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Feb 2024 07:05:40 GMT
USER varnish
# Tue, 13 Feb 2024 07:05:40 GMT
EXPOSE 80 8443
# Tue, 13 Feb 2024 07:05:41 GMT
CMD []
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d331b5369825d3bfa26f9d6f6930e98844fbad063049ccc634b100b73f5b74c`  
		Last Modified: Tue, 13 Feb 2024 07:17:28 GMT  
		Size: 104.5 MB (104535560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691ac9af3a08f9922d69362aa8127711d61a95a7854d163448ad1ee4a7b90863`  
		Last Modified: Tue, 13 Feb 2024 07:17:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:fff33f4348f599b35d8e6918962a059cc988f032e68586dc192a8d0b556998d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112312243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30509136dae50cd98bc572da131490833d214e4baaaa361c252df6427a4736`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:59:59 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 13 Feb 2024 03:59:59 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 13 Feb 2024 04:00:00 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 13 Feb 2024 04:00:00 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 13 Feb 2024 04:00:00 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 13 Feb 2024 04:00:00 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 13 Feb 2024 04:00:00 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 13 Feb 2024 04:00:00 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 13 Feb 2024 04:00:00 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 13 Feb 2024 04:00:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 Feb 2024 04:00:01 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Feb 2024 04:02:42 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Feb 2024 04:02:49 GMT
WORKDIR /etc/varnish
# Tue, 13 Feb 2024 04:02:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 13 Feb 2024 04:02:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Feb 2024 04:02:50 GMT
USER varnish
# Tue, 13 Feb 2024 04:02:50 GMT
EXPOSE 80 8443
# Tue, 13 Feb 2024 04:02:51 GMT
CMD []
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3543f1bdb61cfae5b67645acdddf62ebe6e295c8468c27f4d6c1d616b990f1b0`  
		Last Modified: Tue, 13 Feb 2024 04:12:31 GMT  
		Size: 84.8 MB (84823166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533a2162cbf4c32f760dc4a28675a8446f0f273c696269b73bb386390e388e32`  
		Last Modified: Tue, 13 Feb 2024 04:12:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
