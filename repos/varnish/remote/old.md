## `varnish:old`

```console
$ docker pull varnish@sha256:ac15fe0aee0df53beb019d15a4350916d0e42287be1c9d74d8e64c09da56a6d4
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
$ docker pull varnish@sha256:83655796e18e571ce9b2c9bb4ea15cd835238d88e70c67efc56b3f4418522f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101972165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c68141722a0c9bde224e5a07cbd8d6e1130c23a4df6746d78f29d520abef14a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 09:37:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 12 Mar 2024 09:37:46 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 12 Mar 2024 09:37:46 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 12 Mar 2024 09:37:46 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 12 Mar 2024 09:37:46 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 12 Mar 2024 09:37:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 12 Mar 2024 09:37:46 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 12 Mar 2024 09:37:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 12 Mar 2024 09:37:46 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 12 Mar 2024 09:37:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 12 Mar 2024 09:37:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 12 Mar 2024 09:40:11 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 12 Mar 2024 09:40:12 GMT
WORKDIR /etc/varnish
# Tue, 12 Mar 2024 09:40:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 12 Mar 2024 09:40:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 12 Mar 2024 09:40:12 GMT
USER varnish
# Tue, 12 Mar 2024 09:40:12 GMT
EXPOSE 80 8443
# Tue, 12 Mar 2024 09:40:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821a100bd17aad2e989a630b08f7feb61073a3cf0ed2b3a1ac46aa698a49d19`  
		Last Modified: Tue, 12 Mar 2024 09:43:06 GMT  
		Size: 70.5 MB (70549186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5adc7b9d81aedc97625382f29007c351e0b3ff57be0e763e0f443d844c27a6e`  
		Last Modified: Tue, 12 Mar 2024 09:42:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:b3adaed41992f12a8e078313d06eca53240a06ae86c7ba567a1e323d7c05952e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78759681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1875ab47023978d50d6bfdb4bd25bf65f23abd28dbd290dbd7891ad1054afea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Mar 2024 00:59:38 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Tue, 12 Mar 2024 00:59:38 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:17:20 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 12 Mar 2024 07:17:20 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 12 Mar 2024 07:17:20 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 12 Mar 2024 07:17:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 12 Mar 2024 07:17:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 12 Mar 2024 07:17:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 12 Mar 2024 07:17:21 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 12 Mar 2024 07:17:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 12 Mar 2024 07:17:21 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 12 Mar 2024 07:17:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 12 Mar 2024 07:17:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 12 Mar 2024 07:19:54 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 12 Mar 2024 07:19:55 GMT
WORKDIR /etc/varnish
# Tue, 12 Mar 2024 07:19:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 12 Mar 2024 07:19:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 12 Mar 2024 07:19:55 GMT
USER varnish
# Tue, 12 Mar 2024 07:19:55 GMT
EXPOSE 80 8443
# Tue, 12 Mar 2024 07:19:55 GMT
CMD []
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8b3acae483d8992626eea6e9666b6edf0550d7755430ae074c2308ed455d26`  
		Last Modified: Tue, 12 Mar 2024 07:22:37 GMT  
		Size: 52.2 MB (52176478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22613d8247f85a72a0b4a47e169f92b55d65c584aa67d8a15f0ad667ebf9d37c`  
		Last Modified: Tue, 12 Mar 2024 07:22:31 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:439989ba9939abf6b38e610a1c1d92526d0119810e064bcf2551944ae8a27968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129244185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5103df20372f4922106070d8eeca169886ddd40c2369ffcc6f9e5b43bc6968`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 09:55:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:54:41 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 18:54:41 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 18:54:41 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 18:54:41 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 18:54:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:54:41 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 18:54:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 18:54:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:54:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 19 Mar 2024 18:54:41 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:56:46 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 18:56:48 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:56:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:56:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:56:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:56:48 GMT
USER varnish
# Tue, 19 Mar 2024 18:56:48 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:56:48 GMT
CMD []
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a05a38f8732e4679d885de9111cb411438eaa8b3e966ee6c9537f747b2a1ed`  
		Last Modified: Tue, 19 Mar 2024 19:01:14 GMT  
		Size: 100.1 MB (100085747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c30e06eb43d483a1bcc73212caa5ca6f2015f36e9d367e7d395fbd15fc343d`  
		Last Modified: Tue, 19 Mar 2024 19:01:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a067bdeb49b68ad8cf1878c53de22163cd4829614fb62eef41cbf96c9dc7f1d`  
		Last Modified: Tue, 19 Mar 2024 19:01:03 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:ccb6e0e653b16286a1cf200569eb05154aa49f0fb25557deee7e4a2ec2b52599
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131898971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a634e4ce3620b925ff247649f389ce3377bf8aeb414cffd5a729a8c37f0d0621`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 08:00:38 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:00:35 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:00:35 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:00:35 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:00:35 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:00:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:00:36 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:00:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:00:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:00:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 19 Mar 2024 19:00:36 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:04:05 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:04:07 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:04:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:04:07 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:04:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:04:07 GMT
USER varnish
# Tue, 19 Mar 2024 19:04:07 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:04:08 GMT
CMD []
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea67cc9ed641c67f1ff6edc6238204535377ccc48e4049d16bc15691bbb3f22`  
		Last Modified: Tue, 19 Mar 2024 19:10:47 GMT  
		Size: 101.8 MB (101755084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4f42d0302ce330ddcf1de1f8ca1b7ec88eaa0aa078ca23f05c5183c3cb366b`  
		Last Modified: Tue, 19 Mar 2024 19:10:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2951719b6e731a302fb0528ac4f59d47a8788fbe50961d3346f33369ad089432`  
		Last Modified: Tue, 19 Mar 2024 19:10:25 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:11b1ef7ccfb485c49ca293d02a4d0d59a1f35b7907f9029cb3fd5feefcc29900
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100892579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5299db2435b75c947b75afe3346160d2c6874a97f3ee3f11d5202c3cc4f2615c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 14:51:27 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 12 Mar 2024 14:51:28 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 12 Mar 2024 14:51:29 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 12 Mar 2024 14:51:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 12 Mar 2024 14:51:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 12 Mar 2024 14:51:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 12 Mar 2024 14:51:32 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 12 Mar 2024 14:51:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 12 Mar 2024 14:51:34 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 12 Mar 2024 14:51:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 12 Mar 2024 14:51:35 GMT
ENV VARNISH_SIZE=100M
# Tue, 12 Mar 2024 15:00:05 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 12 Mar 2024 15:00:09 GMT
WORKDIR /etc/varnish
# Tue, 12 Mar 2024 15:00:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 12 Mar 2024 15:00:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 12 Mar 2024 15:00:11 GMT
USER varnish
# Tue, 12 Mar 2024 15:00:12 GMT
EXPOSE 80 8443
# Tue, 12 Mar 2024 15:00:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cbeef47af6f162990accc51d057591ec43c4bbb191d3416857133a03a18e6`  
		Last Modified: Tue, 12 Mar 2024 15:10:20 GMT  
		Size: 65.6 MB (65594080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886487606ee42ba0141007afd621df0df6a32d7eff4e3770bfac4852be0c35`  
		Last Modified: Tue, 12 Mar 2024 15:10:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:0362dc505602f25195c474edfb2379f5e669de30f25e1bd9c7b0f929d1d70adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82342129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1bd490eb1d417237f34c885c47a9ca81684c834caca5d936fbeab84bd3774f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Mar 2024 00:57:49 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
# Tue, 12 Mar 2024 00:57:50 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:41:56 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 12 Mar 2024 04:41:56 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 12 Mar 2024 04:41:56 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 12 Mar 2024 04:41:56 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 12 Mar 2024 04:41:56 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 12 Mar 2024 04:41:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 12 Mar 2024 04:41:56 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 12 Mar 2024 04:41:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 12 Mar 2024 04:41:56 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 12 Mar 2024 04:41:57 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 12 Mar 2024 04:41:57 GMT
ENV VARNISH_SIZE=100M
# Tue, 12 Mar 2024 04:44:06 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 12 Mar 2024 04:44:08 GMT
WORKDIR /etc/varnish
# Tue, 12 Mar 2024 04:44:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:44:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 12 Mar 2024 04:44:08 GMT
USER varnish
# Tue, 12 Mar 2024 04:44:08 GMT
EXPOSE 80 8443
# Tue, 12 Mar 2024 04:44:08 GMT
CMD []
```

-	Layers:
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba30415f9e521907e8d374d3dad4ffd5bda7197d51fb7a8bf29e3c5d7f6a5d44`  
		Last Modified: Tue, 12 Mar 2024 04:49:56 GMT  
		Size: 52.7 MB (52681392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b43476fe943b0d3fb175ede66147f4ecec5bdd7a990e844dcfd4d2d6fb50cf0`  
		Last Modified: Tue, 12 Mar 2024 04:49:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
