## `varnish:latest`

```console
$ docker pull varnish@sha256:6745cc2bd22e5c9d6d3adf59cb60825d4f94091bc57e38f9d4079843a43670ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:f8f6cc5b581e2487fe2cd4c3c9e61ccbf1e92629b3be26473fbbeaea96602483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134456524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4819bbd3b63e64144d2e4e0de799ab7a68a6b8331e64e7fbc32039c8c95f7c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6c2731ec44510207506ca42041f3e5d389d5360fedd00fec776b6e1121808`  
		Last Modified: Tue, 01 Jul 2025 02:27:35 GMT  
		Size: 106.2 MB (106224335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8addd7113860524a5aa53c0a79f7cfeb75f1a9ffbd2eeff37b5e9e5ca35102c`  
		Last Modified: Tue, 01 Jul 2025 02:27:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05d94d0505c6b4e083e3f0e7c7ba6da1e769e59629401aa6c7f847766cc8dd`  
		Last Modified: Tue, 01 Jul 2025 02:27:30 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:76766d482b1d2f226d07b75dc91d6923a61efb514c6329cd6ac775642a2de652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1c648fa56205de3cc02d489259b55686120ad41f2155899872ee451af5e7d9`

```dockerfile
```

-	Layers:
	-	`sha256:2c2fb97bcfd7f4a91d7d62391d0ae6740e1d0271b3b6a7cfee1a39b56bd4200e`  
		Last Modified: Tue, 01 Jul 2025 06:19:43 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:b86c0bfb507a209bb941a9eb5e292f0cb80d6994a9363c5e7fc84a979dde6f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104796024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9149ca33beb7683b197e742189d93ae45baf5a0d104364870f4be7bc161b17a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd74a190feddd0f08939369afb5f715bd04d61bdc6f758f8fb8f784503a5aaf`  
		Last Modified: Wed, 11 Jun 2025 06:20:16 GMT  
		Size: 80.9 MB (80855234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a6b1b3d39af2bca346f24a7f0ae6dbe3c95ac388e6cd99d28ae10388cae498`  
		Last Modified: Wed, 11 Jun 2025 05:00:11 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fffedccedf5b6065f59bf52542d903adc8924564cae473e97832102c5c9e2`  
		Last Modified: Wed, 11 Jun 2025 05:00:16 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:403fa254cc31235d68a7440dae830810517d908ba996164b121b4f5dab1e5542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e40b52ba0215f555ab6d7f9d8f999ec4adbfc1a2c19dfc57d933d6d9cff3e8`

```dockerfile
```

-	Layers:
	-	`sha256:26a1c9db4287772910f294282b932583f94347b5b9f7d02027c985dd8d5d0138`  
		Last Modified: Wed, 11 Jun 2025 06:19:36 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6d5d2f4202a189c2ce12f51a6267516ada6c71915d63607e6e1a17c206fd8b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128772523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a6b8d9de2c571d56965a6d16f192378a1788cad81ea98592c81fcf67e5fb21`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a615e110474c18026be60b1ed71ffdc2bd5ed663d92f11031a9432dcb4d4c7`  
		Last Modified: Wed, 11 Jun 2025 02:51:23 GMT  
		Size: 100.7 MB (100692804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5b00cedf03cbbe7c97ce15c23d0f5c3a0268e3c7506e0606b06a1e7722b535`  
		Last Modified: Wed, 11 Jun 2025 02:51:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dba2d7711cdf0ceea8be6536f9ccc0abb2d91ad198a9735f55ef929d6b4a1c`  
		Last Modified: Wed, 11 Jun 2025 02:51:10 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:fd005f82af986fabea4b93dafbdff51132ace516baac22a53f071570fd203eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1130638c59cf553397070a12b9e7e8e80d2bb2a7cf628ef82e59c7ac871cd1`

```dockerfile
```

-	Layers:
	-	`sha256:c1a858e223d6eae5e059786f46664f922f47ca8b4be3427a8b6a8fef9e96e26f`  
		Last Modified: Wed, 11 Jun 2025 03:19:33 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:39253cc9bbd4657e72e364929b307b79cc857e1afb53ea5eafe297965b01d967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131549481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d517057a70880fe84279ed4549fbbf82a556171851cebc277b2aad93b314cd7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29ea190e921a428ff9447ed7b8f485f882bfa5709e0b191571607be8b69a3f8`  
		Last Modified: Tue, 01 Jul 2025 02:27:03 GMT  
		Size: 102.3 MB (102335005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2754665eb7bf8175c46ab1ab3fa9039b066160eb50ef427b114b27ae98db`  
		Last Modified: Tue, 01 Jul 2025 02:26:55 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570e217e3e88f67eab834b1734b2fe34e32ed2eff3d57183c2a94aba974ab948`  
		Last Modified: Tue, 01 Jul 2025 02:26:55 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:f16a6f91be491733ad0187c3b48240d6ad4468ce99d2e8eb36d527ef6d935c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c294df9e60dc29f798e227f978029b033440108d38626487794fdf754688be4`

```dockerfile
```

-	Layers:
	-	`sha256:843ddef2be6084c422fa423f03b9999d3c1bbf527cc8029fb10280e843f2b135`  
		Last Modified: Tue, 01 Jul 2025 06:19:52 GMT  
		Size: 19.4 KB (19395 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:59af424d92239a886d200934e03f2d88a55470cc70aaab42da9c3a03af16f396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137242597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c644effc2bc7fec86db8a94411861d9207c9ef1112ab273dea06cc02b11a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3c62da167550e8400e3b1eea7dbd1b690b4f8c67b8980795ec5306c9797ef2`  
		Last Modified: Tue, 01 Jul 2025 04:57:29 GMT  
		Size: 105.2 MB (105167728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5b27bcadd51eec1ceab06a0a01a923b698da0cbee13a21076904ea26c76f26`  
		Last Modified: Tue, 01 Jul 2025 04:57:23 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab58e9f4c2ecd3db5d7f63b9dbac7dfccfa798341b19376e483aad74f5125de`  
		Last Modified: Tue, 01 Jul 2025 04:57:23 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:9eff5a004c92828f167d7974be98cacfbcc60e3547358839c50afc3cd6529187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8239c144f9ca8676933ff56f921a4d659e2e9f3ff1fbc327d801ccb364b382`

```dockerfile
```

-	Layers:
	-	`sha256:2b65c6204032589061ccbbb142da8a79017def45750eea1a3240ee9cb3518b2f`  
		Last Modified: Tue, 01 Jul 2025 06:19:56 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:c4e301ceb5d42962b0cd1d69c7caf5659b870aeecfd28a5d9e42c63b1981d5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112367351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818d8a1547f31c2060f8802115847a94f9e6f2ae1c35c2f440b285524473ab1e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba52c2aba54820ed8d1ccc70b7f738700cbb045facc77b6482b0cbb7fb44202`  
		Last Modified: Tue, 01 Jul 2025 05:25:08 GMT  
		Size: 85.5 MB (85477495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9783ac9ace9baf34fb9ebb85b75ca9c8fc20434cf758e4bd0d1f66fca09a6`  
		Last Modified: Tue, 01 Jul 2025 05:24:54 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fef114fc055791295e8c5d472dbe27ebcf9368dd91fed89c56fe015de2fa9c`  
		Last Modified: Tue, 01 Jul 2025 05:24:54 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:46058d028384f35127983fd06e6423aad5f003af52fd74c8922f1e4eb4256ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5049592be8667a7d68f745fd5f1c0067f0eb8a494337745dd3773a6f5d1a55c`

```dockerfile
```

-	Layers:
	-	`sha256:a222aa246ef8168d9b6988ff5dbd0a21d99c6e5de078f35a3bf9e2b33d8cfdad`  
		Last Modified: Tue, 01 Jul 2025 06:19:59 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json
