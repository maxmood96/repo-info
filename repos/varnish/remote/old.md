## `varnish:old`

```console
$ docker pull varnish@sha256:ae13892c5aaf290ea147046d01e9422751ea43631ae856568660e01f33528ed3
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
$ docker pull varnish@sha256:74c8a55fa6c480a7e60d36822597ea5ada38934b5e94ffd3afafa31f4112fe7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101976335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83abf1a7809514fb8fdfcac84aac6565d1cbfb19c9d47c877733b720de28f1bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:19:23 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Tue, 04 Jul 2023 03:19:23 GMT
ARG VARNISH_VERSION=7.2.1
# Tue, 04 Jul 2023 03:19:23 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Tue, 04 Jul 2023 03:19:23 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Tue, 04 Jul 2023 03:19:23 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Tue, 04 Jul 2023 03:19:23 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 04 Jul 2023 03:19:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Tue, 04 Jul 2023 03:19:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Tue, 11 Jul 2023 18:24:38 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 11 Jul 2023 18:24:38 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Tue, 11 Jul 2023 18:24:38 GMT
ENV VARNISH_SIZE=100M
# Tue, 11 Jul 2023 18:26:47 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 11 Jul 2023 18:26:47 GMT
WORKDIR /etc/varnish
# Tue, 11 Jul 2023 18:26:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 11 Jul 2023 18:26:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 11 Jul 2023 18:26:48 GMT
USER varnish
# Tue, 11 Jul 2023 18:26:48 GMT
EXPOSE 80 8443
# Tue, 11 Jul 2023 18:26:48 GMT
CMD []
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88e0f5d2ec1acefef4cb6f51daf4673b23b993de7f6d8a7ab4acc57e9784722`  
		Last Modified: Tue, 11 Jul 2023 18:29:29 GMT  
		Size: 70.6 MB (70558456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754ab83be516554351c0ffc17718c92951a5130b9bcdb4646fda9c4f65687c9f`  
		Last Modified: Tue, 11 Jul 2023 18:29:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:8acb5ba81cf5d495efddff1a343c0b18573d6d434266442b7cb8e9dc9e52c23a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78756374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a17263c47006b23066241407fa4872a792f562fbe4981ca50c7d533ade3e908`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:40:50 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Tue, 04 Jul 2023 05:40:50 GMT
ARG VARNISH_VERSION=7.2.1
# Tue, 04 Jul 2023 05:40:50 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Tue, 04 Jul 2023 05:40:50 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Tue, 04 Jul 2023 05:40:51 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Tue, 04 Jul 2023 05:40:51 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 04 Jul 2023 05:40:51 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Tue, 04 Jul 2023 05:40:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Tue, 11 Jul 2023 18:17:32 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 11 Jul 2023 18:17:32 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Tue, 11 Jul 2023 18:17:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 11 Jul 2023 18:19:39 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 11 Jul 2023 18:19:40 GMT
WORKDIR /etc/varnish
# Tue, 11 Jul 2023 18:19:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 11 Jul 2023 18:19:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 11 Jul 2023 18:19:40 GMT
USER varnish
# Tue, 11 Jul 2023 18:19:40 GMT
EXPOSE 80 8443
# Tue, 11 Jul 2023 18:19:40 GMT
CMD []
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a394c9f9ea8f68035b92092deee8eb1193ceb50e5cf936e785f024fbc40165`  
		Last Modified: Tue, 11 Jul 2023 18:22:17 GMT  
		Size: 52.2 MB (52177130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0969c8924eafcd75229e9ec58901966bf4fb65a6f7f3d67cd06b6e5e8ae9fb8`  
		Last Modified: Tue, 11 Jul 2023 18:22:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:55f86fb67ada77f34cfed898fc4c1a965d8966b4652485f7f47181cee1ab8a0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96022501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0fd8a716331e2b747cbd3104de25bbee55789f13ba1f2ce91e43afdf5bea0c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:49:42 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Fri, 28 Jul 2023 01:49:42 GMT
ARG VARNISH_VERSION=7.2.1
# Fri, 28 Jul 2023 01:49:42 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Fri, 28 Jul 2023 01:49:42 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Fri, 28 Jul 2023 01:49:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Fri, 28 Jul 2023 01:49:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Fri, 28 Jul 2023 01:49:42 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Fri, 28 Jul 2023 01:49:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Fri, 28 Jul 2023 01:49:42 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Fri, 28 Jul 2023 01:49:42 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Fri, 28 Jul 2023 01:49:42 GMT
ENV VARNISH_SIZE=100M
# Fri, 28 Jul 2023 01:51:41 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Fri, 28 Jul 2023 01:51:41 GMT
WORKDIR /etc/varnish
# Fri, 28 Jul 2023 01:51:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:51:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 28 Jul 2023 01:51:42 GMT
USER varnish
# Fri, 28 Jul 2023 01:51:42 GMT
EXPOSE 80 8443
# Fri, 28 Jul 2023 01:51:42 GMT
CMD []
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fe1745c972857ca276fa5ce2aec1764beb4b5b990dcc4e53c313d6928bd26a`  
		Last Modified: Fri, 28 Jul 2023 01:54:06 GMT  
		Size: 66.0 MB (65959176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc288fee5ab9b3d91b48e5e79822aaa694ea0a14f97f0758e844944668d4b209`  
		Last Modified: Fri, 28 Jul 2023 01:53:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:466dae102541010b7dbfd6654855c56f61569b8999d872ef4e803b0d32da6a5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103211593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f72216d5ddaaaf1b0ed9e30564ae395f0cc9a2aa42d393b27902169cc7d118d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:38:59 GMT
ADD file:c39e332ccb9cb890ba7896a09e9f074b3c8d67094b4eaf73d5c67e8949c2e0be in / 
# Tue, 04 Jul 2023 01:39:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 09:04:18 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Tue, 04 Jul 2023 09:04:18 GMT
ARG VARNISH_VERSION=7.2.1
# Tue, 04 Jul 2023 09:04:18 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Tue, 04 Jul 2023 09:04:18 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Tue, 04 Jul 2023 09:04:18 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Tue, 04 Jul 2023 09:04:18 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 04 Jul 2023 09:04:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Tue, 04 Jul 2023 09:04:19 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Tue, 11 Jul 2023 18:44:17 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 11 Jul 2023 18:44:18 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Tue, 11 Jul 2023 18:44:18 GMT
ENV VARNISH_SIZE=100M
# Tue, 11 Jul 2023 18:47:10 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 11 Jul 2023 18:47:11 GMT
WORKDIR /etc/varnish
# Tue, 11 Jul 2023 18:47:11 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 11 Jul 2023 18:47:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 11 Jul 2023 18:47:11 GMT
USER varnish
# Tue, 11 Jul 2023 18:47:11 GMT
EXPOSE 80 8443
# Tue, 11 Jul 2023 18:47:11 GMT
CMD []
```

-	Layers:
	-	`sha256:3466e7f9e8ec982697fc130dbb1706d708f5c53e348a638019a955c15c7395af`  
		Last Modified: Tue, 04 Jul 2023 01:44:12 GMT  
		Size: 32.4 MB (32397496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a86b46744cff6a7fef3997485ae61ca48e0b734c37353062317b3d5d718d50`  
		Last Modified: Tue, 11 Jul 2023 18:50:48 GMT  
		Size: 70.8 MB (70813606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76ccbd9ff33b0cc10791dd0e0f25b97280e3911c993e89a92354b8d1ea6501d`  
		Last Modified: Tue, 11 Jul 2023 18:50:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:fc4b8cff97c951327875c3171efacc0b16da8f9cb9a0e3f6031d203685db2b1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100896173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc133bd96e6207343f489bb1a708059561b023a782ad44aff0760f7c4c9b00eb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:36:04 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Fri, 28 Jul 2023 01:36:05 GMT
ARG VARNISH_VERSION=7.2.1
# Fri, 28 Jul 2023 01:36:05 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Fri, 28 Jul 2023 01:36:05 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Fri, 28 Jul 2023 01:36:05 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Fri, 28 Jul 2023 01:36:05 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Fri, 28 Jul 2023 01:36:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Fri, 28 Jul 2023 01:36:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Fri, 28 Jul 2023 01:36:06 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Fri, 28 Jul 2023 01:36:06 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Fri, 28 Jul 2023 01:36:07 GMT
ENV VARNISH_SIZE=100M
# Fri, 28 Jul 2023 01:40:47 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Fri, 28 Jul 2023 01:40:50 GMT
WORKDIR /etc/varnish
# Fri, 28 Jul 2023 01:40:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:40:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 28 Jul 2023 01:40:51 GMT
USER varnish
# Fri, 28 Jul 2023 01:40:51 GMT
EXPOSE 80 8443
# Fri, 28 Jul 2023 01:40:51 GMT
CMD []
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e1a88b4e4366b5bb3eab1b0cc0ebfd4f2049b3a79cbfe3e11b7c61e372e50`  
		Last Modified: Fri, 28 Jul 2023 01:46:26 GMT  
		Size: 65.6 MB (65604649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6957e82603bd5d6b8facaff79aaa8a008875ba2e1ca4e41cdb3a6e62ccf0f153`  
		Last Modified: Fri, 28 Jul 2023 01:46:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:8cfc9b9bc5eaf438a74c931d4575b9a1097d18c56261a1ebd6e42f3959a2b55f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82323837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ed4fcf8f9fcdc7a97735c3c7f79be3377fe70a703004be056f5a3bb61fd42a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:18:30 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Fri, 28 Jul 2023 03:18:30 GMT
ARG VARNISH_VERSION=7.2.1
# Fri, 28 Jul 2023 03:18:30 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Fri, 28 Jul 2023 03:18:30 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Fri, 28 Jul 2023 03:18:30 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Fri, 28 Jul 2023 03:18:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Fri, 28 Jul 2023 03:18:30 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Fri, 28 Jul 2023 03:18:30 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Fri, 28 Jul 2023 03:18:30 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Fri, 28 Jul 2023 03:18:31 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Fri, 28 Jul 2023 03:18:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 28 Jul 2023 03:20:34 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Fri, 28 Jul 2023 03:20:36 GMT
WORKDIR /etc/varnish
# Fri, 28 Jul 2023 03:20:36 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 28 Jul 2023 03:20:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 28 Jul 2023 03:20:36 GMT
USER varnish
# Fri, 28 Jul 2023 03:20:36 GMT
EXPOSE 80 8443
# Fri, 28 Jul 2023 03:20:36 GMT
CMD []
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e547a5422bd6388581eb6cacb1a2444d6866f06b83a8d058f13eb0ac157cb2b9`  
		Last Modified: Fri, 28 Jul 2023 03:23:09 GMT  
		Size: 52.7 MB (52670463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db949192b2fd82ead342bba93463eba585f3dfc3ccda945cbd4f56d03f4f0766`  
		Last Modified: Fri, 28 Jul 2023 03:23:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
