## `varnish:fresh`

```console
$ docker pull varnish@sha256:baa5e41f4042965099c01698e6020337e783abda8f7b4842abb67c2c14e6cd8e
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
$ docker pull varnish@sha256:e03566ef6752192c478b1aa7bba603dc26f1ee563934c03f28e9c6a7a5396d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134737591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266771d9cf5c42149096e6813c1b152608a114703951e87c69ce3220c862ab70`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 21:27:13 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Wed, 11 Oct 2023 21:27:13 GMT
ARG VARNISH_VERSION=7.4.1
# Wed, 11 Oct 2023 21:27:13 GMT
ARG DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c
# Wed, 11 Oct 2023 21:27:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 11 Oct 2023 21:27:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 11 Oct 2023 21:27:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Wed, 11 Oct 2023 21:27:14 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Wed, 11 Oct 2023 21:27:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Wed, 11 Oct 2023 21:27:14 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Wed, 11 Oct 2023 21:27:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Wed, 11 Oct 2023 21:27:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 11 Oct 2023 21:30:00 GMT
# ARGS: DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.1 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.1.tgz -o $tmpdir/orig.tgz;     echo "d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 11 Oct 2023 21:30:01 GMT
WORKDIR /etc/varnish
# Wed, 11 Oct 2023 21:30:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 11 Oct 2023 21:30:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 11 Oct 2023 21:30:01 GMT
USER varnish
# Wed, 11 Oct 2023 21:30:01 GMT
EXPOSE 80 8443
# Wed, 11 Oct 2023 21:30:01 GMT
CMD []
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d3b02baeacb05096f1d533167545798575b4b39a4f516a201ad8a3c0fd9e0`  
		Last Modified: Wed, 11 Oct 2023 21:35:14 GMT  
		Size: 105.6 MB (105587228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88afe6700045cede25a79c7cae3b4fd9c2630ea13c3445c62ee292dc732123`  
		Last Modified: Wed, 11 Oct 2023 21:34:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9f1ee90ca7e38b7734aae5cb006091d09111ec90fb5c47f2a17254c8bc5db27d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105035622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1b8ee06cc65306a09f1feae6089bc4113cf8a2f83bba549f495b3f62bf280a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:20:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Wed, 01 Nov 2023 02:20:49 GMT
ARG VARNISH_VERSION=7.4.1
# Wed, 01 Nov 2023 02:20:49 GMT
ARG DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c
# Wed, 01 Nov 2023 02:20:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 01 Nov 2023 02:20:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 01 Nov 2023 02:20:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Wed, 01 Nov 2023 02:20:49 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Wed, 01 Nov 2023 02:20:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Wed, 01 Nov 2023 02:20:49 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Wed, 01 Nov 2023 02:20:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Wed, 01 Nov 2023 02:20:50 GMT
ENV VARNISH_SIZE=100M
# Wed, 01 Nov 2023 02:23:35 GMT
# ARGS: DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.1 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.1.tgz -o $tmpdir/orig.tgz;     echo "d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 01 Nov 2023 02:23:36 GMT
WORKDIR /etc/varnish
# Wed, 01 Nov 2023 02:23:36 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 01 Nov 2023 02:23:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 01 Nov 2023 02:23:36 GMT
USER varnish
# Wed, 01 Nov 2023 02:23:36 GMT
EXPOSE 80 8443
# Wed, 01 Nov 2023 02:23:36 GMT
CMD []
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d2a0f9e6bceceeb9347fea5914db7cbaf5442cdb8f6d1850335f7569a79164`  
		Last Modified: Wed, 01 Nov 2023 02:28:54 GMT  
		Size: 80.3 MB (80286231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72abcd16f0021f39ebb8e1ffdad51ec1ad1841a4184009d3ce3440fac5a74c13`  
		Last Modified: Wed, 01 Nov 2023 02:28:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7a72ab24d4fa062d4824f8277f8d58ccbf3823c592c701208502113640a76d02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129224693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975cff80172e677179351e86e12917d23644d70222cd5b6a79ba12a7d4be837d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:53:16 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Wed, 01 Nov 2023 01:53:16 GMT
ARG VARNISH_VERSION=7.4.1
# Wed, 01 Nov 2023 01:53:16 GMT
ARG DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c
# Wed, 01 Nov 2023 01:53:16 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 01 Nov 2023 01:53:16 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 01 Nov 2023 01:53:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Wed, 01 Nov 2023 01:53:16 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Wed, 01 Nov 2023 01:53:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Wed, 01 Nov 2023 01:53:16 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Wed, 01 Nov 2023 01:53:17 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Wed, 01 Nov 2023 01:53:17 GMT
ENV VARNISH_SIZE=100M
# Wed, 01 Nov 2023 01:55:43 GMT
# ARGS: DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.1 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.1.tgz -o $tmpdir/orig.tgz;     echo "d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 01 Nov 2023 01:55:44 GMT
WORKDIR /etc/varnish
# Wed, 01 Nov 2023 01:55:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 01 Nov 2023 01:55:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 01 Nov 2023 01:55:44 GMT
USER varnish
# Wed, 01 Nov 2023 01:55:45 GMT
EXPOSE 80 8443
# Wed, 01 Nov 2023 01:55:45 GMT
CMD []
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9289feae89d0119d9843e26e06083d39715e526b8b976ab41e84b12206ce0`  
		Last Modified: Wed, 01 Nov 2023 02:00:25 GMT  
		Size: 100.0 MB (100045082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a440ccc67e63c46a820591839f5fc5f0da86fbd32e181b42d3f9a10b9e150a3b`  
		Last Modified: Wed, 01 Nov 2023 02:00:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:b0b281bd04e70c06c4d95562ddc165603c7fcb63797a5307ea577d0854a46ba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131877976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8763c9a49d7d742b60afd31d81ea0e3816bba8e58111f0d3bfc26b36fc3c66f5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 11 Oct 2023 17:40:42 GMT
ADD file:31318c1b1f05d559cce42f5b12eef97d916932217e0b987fb07c0fc11bf0a14a in / 
# Wed, 11 Oct 2023 17:40:42 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 08:38:19 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 12 Oct 2023 08:38:19 GMT
ARG VARNISH_VERSION=7.4.1
# Thu, 12 Oct 2023 08:38:20 GMT
ARG DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c
# Thu, 12 Oct 2023 08:38:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 12 Oct 2023 08:38:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 12 Oct 2023 08:38:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 12 Oct 2023 08:38:20 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Thu, 12 Oct 2023 08:38:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Thu, 12 Oct 2023 08:38:20 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Thu, 12 Oct 2023 08:38:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 12 Oct 2023 08:38:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 12 Oct 2023 08:42:04 GMT
# ARGS: DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.1 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.1.tgz -o $tmpdir/orig.tgz;     echo "d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 12 Oct 2023 08:42:05 GMT
WORKDIR /etc/varnish
# Thu, 12 Oct 2023 08:42:05 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 12 Oct 2023 08:42:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 12 Oct 2023 08:42:06 GMT
USER varnish
# Thu, 12 Oct 2023 08:42:06 GMT
EXPOSE 80 8443
# Thu, 12 Oct 2023 08:42:06 GMT
CMD []
```

-	Layers:
	-	`sha256:b27d0f1369837277a82877763487cdd2535037988fc27e16f11cf74e103ae4cd`  
		Last Modified: Wed, 11 Oct 2023 17:45:31 GMT  
		Size: 30.2 MB (30164118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4d7224a6538ed66733bc96ac79177a58d0039e0e68594173cc295e2ea9b504`  
		Last Modified: Thu, 12 Oct 2023 08:48:35 GMT  
		Size: 101.7 MB (101713366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621ed1744001a5b482de115c1a397507d44f792c45cdd41dce56ecb1fca9cbe3`  
		Last Modified: Thu, 12 Oct 2023 08:48:15 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:b8eef7fae1f322326bbe807f1c611ad982a147355975c3815deb2ce3d89ee1c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137667558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76aa22961b08a846818920fbe0ccb6a8a469038f2efe29fd526f76068b5ad3f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 01 Nov 2023 00:21:39 GMT
ADD file:f36d600ab8508979b5763875a75f35555fa0a83d2656cbcdfa50978c6ae97353 in / 
# Wed, 01 Nov 2023 00:21:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:03:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Wed, 01 Nov 2023 01:03:47 GMT
ARG VARNISH_VERSION=7.4.1
# Wed, 01 Nov 2023 01:03:47 GMT
ARG DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c
# Wed, 01 Nov 2023 01:03:48 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 01 Nov 2023 01:03:48 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 01 Nov 2023 01:03:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Wed, 01 Nov 2023 01:03:49 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Wed, 01 Nov 2023 01:03:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Wed, 01 Nov 2023 01:03:49 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Wed, 01 Nov 2023 01:03:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Wed, 01 Nov 2023 01:03:50 GMT
ENV VARNISH_SIZE=100M
# Wed, 01 Nov 2023 01:11:10 GMT
# ARGS: DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.1 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.1.tgz -o $tmpdir/orig.tgz;     echo "d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 01 Nov 2023 01:11:20 GMT
WORKDIR /etc/varnish
# Wed, 01 Nov 2023 01:11:21 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 01 Nov 2023 01:11:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 01 Nov 2023 01:11:23 GMT
USER varnish
# Wed, 01 Nov 2023 01:11:25 GMT
EXPOSE 80 8443
# Wed, 01 Nov 2023 01:11:26 GMT
CMD []
```

-	Layers:
	-	`sha256:e56c8f20d7d119ff87eb044f21bfd5a4b30bf8436fc5fac12871095a6bd1517c`  
		Last Modified: Wed, 01 Nov 2023 00:26:10 GMT  
		Size: 33.1 MB (33141482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116e260538ae6a8a9193a2ecd262456147a8fb77d87191be7e8c94f3542e79b3`  
		Last Modified: Wed, 01 Nov 2023 01:22:34 GMT  
		Size: 104.5 MB (104525584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3203fae7ec0e38ea3be34ef380e18bbf6def105b20850f16049ddde0a32be756`  
		Last Modified: Wed, 01 Nov 2023 01:22:17 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:0705d9f532875fad97780d55c04f40b844d5dab353cfb2f714af78606519bf97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112329857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c01efe9c0763743e33acb4c63e8825e8098266f7432ebdc5d2b396e892ede4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 01 Nov 2023 00:42:36 GMT
ADD file:2764e93c5bba50564937cce7bcaa7c7d3bdc3fd0d53a7bb09e6955e6fda8d7c2 in / 
# Wed, 01 Nov 2023 00:42:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:37:14 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Wed, 01 Nov 2023 01:37:14 GMT
ARG VARNISH_VERSION=7.4.1
# Wed, 01 Nov 2023 01:37:15 GMT
ARG DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c
# Wed, 01 Nov 2023 01:37:15 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 01 Nov 2023 01:37:15 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 01 Nov 2023 01:37:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Wed, 01 Nov 2023 01:37:15 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Wed, 01 Nov 2023 01:37:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Wed, 01 Nov 2023 01:37:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Wed, 01 Nov 2023 01:37:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Wed, 01 Nov 2023 01:37:16 GMT
ENV VARNISH_SIZE=100M
# Wed, 01 Nov 2023 01:39:44 GMT
# ARGS: DIST_SHA512=d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.1 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.1.tgz -o $tmpdir/orig.tgz;     echo "d5a6ce53bd5fd2afc6a56b7d64fbaf3688bf3de1f39149fb4b4b40acda987bd9ead32f1b9050441a6281c0c2f4a5849d179bfa8615ec98640d9a2e030b0cdb0c  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 01 Nov 2023 01:39:50 GMT
WORKDIR /etc/varnish
# Wed, 01 Nov 2023 01:39:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 01 Nov 2023 01:39:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 01 Nov 2023 01:39:50 GMT
USER varnish
# Wed, 01 Nov 2023 01:39:50 GMT
EXPOSE 80 8443
# Wed, 01 Nov 2023 01:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ac72f5406002214602d5a625a21b606af78a78e99e377d3140a83021f7edd666`  
		Last Modified: Wed, 01 Nov 2023 00:48:04 GMT  
		Size: 27.5 MB (27512766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0926ee316da488d4269f58de23e78d4cbf55f838027c80d9e011eba7ed3c0b`  
		Last Modified: Wed, 01 Nov 2023 01:45:14 GMT  
		Size: 84.8 MB (84816599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60e97a662a16d9db817bc84cc134214704ea8f50dab9d4166873afa2b7459e`  
		Last Modified: Wed, 01 Nov 2023 01:45:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
