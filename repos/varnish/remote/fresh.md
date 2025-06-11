## `varnish:fresh`

```console
$ docker pull varnish@sha256:97bbe53b53547f8ae5325a40f1bef1b302f919f6124cd9ac84c1f332ad3cefbd
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

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:1fb406f0f1a96c7096e36e809df46f77affdce84a0f0be4207e2ff54b203dcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134457072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64edd066293887b96c4ce07fdf8df907b445709b02d263b7280f445c7648211`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5744ff3d2e23d34d0743089bf59ba5f2748ec2c5fec26775186bc337377e851b`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 106.2 MB (106224904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e164cf0b661c869eaece30cba0e61be2086848357e3c4a7da25b774068f58d93`  
		Last Modified: Tue, 10 Jun 2025 23:39:24 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798890658db8b75211d922f379e605b133aa8f037966db845402b2051233dc3b`  
		Last Modified: Tue, 10 Jun 2025 23:39:25 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:cb2e51ef8d92ecd065d728d95ab1923a80135660105960dd535642004393b6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35eb7a48e1fa8ac02e9bd73409fa9b6d24b54b10949b7bb47ae8f1f5f2585e1`

```dockerfile
```

-	Layers:
	-	`sha256:d137545b7fd9769436a46ea420a5af39ed784578a097fea23118e6c29476847e`  
		Last Modified: Wed, 11 Jun 2025 00:19:30 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5adad43b24036dbfff7474871216e581e0f1ac239aae7a5ded6d46705b7e8097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104790091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ace5306343f8f372161bfe6312bf13a01a004a288a36ac30070743f2a489147`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30229820e749488a19247acc507e6395d091a58c8bf65f1818707ad0f4a307`  
		Last Modified: Tue, 27 May 2025 18:59:04 GMT  
		Size: 80.9 MB (80855126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd9115dbc57e1b42e5ba709ec4ec2807eb9a50fd3e6d2460c106f489280f158`  
		Last Modified: Sat, 07 Jun 2025 07:33:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf65c592a8ab18cefe44951bf16df3da586b71b750efe60c9879de33f73ea21`  
		Last Modified: Sat, 07 Jun 2025 07:33:10 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b56c0842d33dfc4ab663a429347398c7bbc9ea2c4904f99075b8cb63a63c2f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab92fe2dbdee6486b9ad4acb5ad3f224e76f7aed8d4bede985fa0e7281faa1`

```dockerfile
```

-	Layers:
	-	`sha256:8d9dc94a2f49cd77f3213c5da639c8685cc2cff303a554713fe278c9159b616e`  
		Last Modified: Wed, 11 Jun 2025 00:19:34 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:00c0a51d4e847dbcae4818cd5705288e034e2257788300ca652fe063e276628a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128760086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffb9b857a68c7e4f59244b933747d6ea1c8fb35e5baa72535574e14c9419f27`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12730279417dd69cef972ec5f2b55b4b294921b01a7469ca63af84171eae00d2`  
		Last Modified: Tue, 03 Jun 2025 13:47:05 GMT  
		Size: 100.7 MB (100692758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87b3d7e17957278d1d7c3a52897534cb3073dd7602eeb1350dbd3e1d930ea2`  
		Last Modified: Tue, 03 Jun 2025 13:46:55 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a484d3e501e2f0894b2b27227423bc6f6c36eea9a3bf739b86ec761286d2b49`  
		Last Modified: Tue, 03 Jun 2025 13:46:55 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:e561bfec36aa85c4972b3d7dd514eb0776a7482ac777e3fa57d520ccd4613de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8cc00168adf4275e765c5f27187726750d0c7dccffdf28c41b56978706d5f5`

```dockerfile
```

-	Layers:
	-	`sha256:31532e1709c6ae0c6931dcb4149082a378390d4cd52c9579acf65597778f12a3`  
		Last Modified: Wed, 11 Jun 2025 00:19:37 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:7a2d031d08c221dae9af6f89de51935b89602c88cb9e338fa38ac2d9cf2fb4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131541794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b1b0917c2ce78d6638ed1594acb1e6252e23d6af92458e85db9bdf5d3f14e7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792795bea6aa08a9c0095496694ef2894b72c3722d00c261d575f3357481497`  
		Last Modified: Tue, 10 Jun 2025 23:38:33 GMT  
		Size: 102.3 MB (102327317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f618a2b09c1d62bd03c0fb3bc2e25052716d9b06f6df255c8e13e8f338f202`  
		Last Modified: Tue, 10 Jun 2025 23:38:29 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d0598fe3df94cd6a01c1afc2ac5370ed8935795caad3a701f7ef59db96e01`  
		Last Modified: Tue, 10 Jun 2025 23:38:28 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:5327eb7d8a659516bc7d5afdd75a14ebddf4a27b1e859bd1392ec42bc3da4aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d345c1ea5cdcd1e97b66447817e4306e2f9c0983fde92a1da38f58aaae6917dd`

```dockerfile
```

-	Layers:
	-	`sha256:992c6f98359aae40f4c85c7a951e3ebbf3aee879c139e313e582b1db725863fb`  
		Last Modified: Wed, 11 Jun 2025 00:19:42 GMT  
		Size: 19.4 KB (19395 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:32c65771f14c4dc222e398b7068c921d81a53bfb0b494beaf07ede68eddafff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137232766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de28949ae9f3a71128d9cae23a968f9e0b31dd25da40a95f63e67c7a02cdf03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad9fb7d959d67ddbc6ce52e903e5bb78a181d3e4f50b6eddc9946adfae26ab`  
		Last Modified: Tue, 27 May 2025 19:00:30 GMT  
		Size: 105.2 MB (105163810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3970c01dab3668d03df86eda7bb409ae65363ece57267731e2de261fce614`  
		Last Modified: Tue, 27 May 2025 19:00:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0e12b051ff2f47ea0eeaa135ec56ebfbc03c079f02669b6b12364d8ab6a70e`  
		Last Modified: Tue, 27 May 2025 19:00:26 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:964458376f5a6a54298e22e5572c911bec2112be613f6845d972200604806af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4711662ae54368511493525ade8531cbb82055836b7a6a048ac091dbcb118a`

```dockerfile
```

-	Layers:
	-	`sha256:4fc124ca8224f765da74cd04a5f5b9094f5b26bb5b4fb5c794a75d516f414cb8`  
		Last Modified: Wed, 11 Jun 2025 00:19:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:c6e237deb92ab2fed552a25134e447b18497e0ef468b0e2f6a86def67e76e843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112358895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c715f4eee9915a912037374a47ff1ae10e965f58f5d75242d25b31fbdfdf33c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ee3cd500b0d134c347f216138fe156e9af9dd384b167e5e4b17e99927ca84`  
		Last Modified: Tue, 27 May 2025 18:59:38 GMT  
		Size: 85.5 MB (85474040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825e56e3ac79ac2de77cbed78e8bf88a9b9922686fb6a81ab268add5846c10d3`  
		Last Modified: Tue, 27 May 2025 18:59:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d2a42fb17f502b8574c68b7ac4c815a9af109b1b7045b4f3d7fbab41e9b3c2`  
		Last Modified: Tue, 27 May 2025 18:59:37 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:531b739ef3576c5f02894c2915605bbf06edde3689104b5664c1b259c8776228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07cbc3f17aebf7b7ada5903f3216fc693b971ef6dcdec8f3a1365c8bc99652e`

```dockerfile
```

-	Layers:
	-	`sha256:673267f767cabf379bed16a8c2dcbb9a6131dbca8761eaef19242141c1502813`  
		Last Modified: Wed, 11 Jun 2025 00:19:50 GMT  
		Size: 19.4 KB (19428 bytes)  
		MIME: application/vnd.in-toto+json
