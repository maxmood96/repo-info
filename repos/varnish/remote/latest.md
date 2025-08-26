## `varnish:latest`

```console
$ docker pull varnish@sha256:1c817b3c2a90d3f2c20fc260e130db8fa33903406a81390b801692330fcc3afd
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
$ docker pull varnish@sha256:b0b5ac26964cea2da515303bc00b688f5f3cee0c3ace843a1b82f46ac47d5554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7c434bc96a63601b4b65c5ba041cefbbdf421a7e223570b0c07e9934f43dc9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.7.2
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
WORKDIR /etc/varnish
# Mon, 25 Aug 2025 17:58:49 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 25 Aug 2025 17:58:49 GMT
USER varnish
# Mon, 25 Aug 2025 17:58:49 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 25 Aug 2025 17:58:49 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f9dd006165d6586f19b0cc49af3aafb44b0bd43e8eb2a7d9954d166714077`  
		Last Modified: Mon, 25 Aug 2025 20:20:12 GMT  
		Size: 86.6 MB (86565240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4614469da07bd073b3038288737d857a82e0b222527b72cb7a8f82baff0ea5db`  
		Last Modified: Mon, 25 Aug 2025 20:20:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a02bfaecc2b8f49d7f8a8fb439fffe3fc9ae93bc37fdf5bee0550995d547e7a`  
		Last Modified: Mon, 25 Aug 2025 20:20:08 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:41e7463157aae5653a29c2614ac3456daabad4896c2feae4d0d931f885fe722c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460fea730ae12a8031bfefc1b5c76adf7d3d7dd1b21675ab5b8c5094f413adb7`

```dockerfile
```

-	Layers:
	-	`sha256:08fa29f7bfa4b34d6e04e63512993460d080177fad402d4953fda0aa990384e1`  
		Last Modified: Mon, 25 Aug 2025 21:19:24 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fdd0813bb8bda49f2c15d98572718ded7fa7b50f22ae53286b16f805d25eecca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82348978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dacda5e9e12871cbc64708c02ec9aeb7347973091afc6103954713d9c78e359`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 22:43:35 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VARNISH_VERSION=7.7.2
# Mon, 18 Aug 2025 22:43:35 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 18 Aug 2025 22:43:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 18 Aug 2025 22:43:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 18 Aug 2025 22:43:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 18 Aug 2025 22:43:35 GMT
ENV VSM_NOPID=1
# Mon, 18 Aug 2025 22:43:35 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 18 Aug 2025 22:43:35 GMT
WORKDIR /etc/varnish
# Mon, 18 Aug 2025 22:43:35 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 22:43:35 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 18 Aug 2025 22:43:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 18 Aug 2025 22:43:35 GMT
USER varnish
# Mon, 18 Aug 2025 22:43:35 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 18 Aug 2025 22:43:35 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07059a257e8d1667d350cdedcc3838274f91848900fe51849b3481b442e28f7a`  
		Last Modified: Mon, 18 Aug 2025 23:12:38 GMT  
		Size: 58.4 MB (58408002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dee1973da0de020448f01313b2a88ce84bf35244a6000b6a2e70f7dde22b7ff`  
		Last Modified: Mon, 18 Aug 2025 23:12:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eee92e0cc1337213b06cb09bdc351b6d084b58cb4f99284895c14c52605b58`  
		Last Modified: Mon, 18 Aug 2025 23:12:38 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:9a9c4c1e12b889745631f2351f6ad3ff6079bcae31ee3330d8969b8faef1a321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4b39335ae52ce2e8300ef5023cece87a82830b00a0e874f9117652671a6ed8`

```dockerfile
```

-	Layers:
	-	`sha256:96b5a52971e188ac1ca302cebff727938342dd5be4fccecd87d8dbac29853f6c`  
		Last Modified: Tue, 19 Aug 2025 00:19:43 GMT  
		Size: 19.6 KB (19560 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ed4e693a69355ed50b000d62a80caed121ca78a1e60bdc5052edaba78a413c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d7d70f5d00f7c38755a662c18a9a1cb89f4447686ec3d9ce67a1c29fbc4c1b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.7.2
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
WORKDIR /etc/varnish
# Mon, 25 Aug 2025 17:58:49 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 25 Aug 2025 17:58:49 GMT
USER varnish
# Mon, 25 Aug 2025 17:58:49 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 25 Aug 2025 17:58:49 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40f9430b4d55ebb3fb93bcf69b123c20705fa97485b021e132ebfe74a553f04`  
		Last Modified: Mon, 25 Aug 2025 21:17:56 GMT  
		Size: 80.4 MB (80381311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4681ec5dd2f7afa805d296e848d7860de33e57d7e798e51a52e1c8244a8ba4b4`  
		Last Modified: Mon, 25 Aug 2025 21:17:48 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385e3cf3592a13c36f4f8c7d744c1af37c3a1a96c0c72ff57d5ec6969a463565`  
		Last Modified: Mon, 25 Aug 2025 21:17:48 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:fb4a813858ba31889881d886a7b6b33b4c52ddbbb545a72091d2d53b4d2ba951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ce70942024377169ddbc440fe19b68bf27b9d572dabca538f4b040cb55a189`

```dockerfile
```

-	Layers:
	-	`sha256:0c803542f133e11b53dcff168697f344b93fee69c1149a593fa361472f75fee6`  
		Last Modified: Tue, 26 Aug 2025 00:19:30 GMT  
		Size: 19.8 KB (19769 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:54dcfa4ec039381d947b1a2374d1387916e85254a02b8b2539cb41593445b72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114476901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c39a8e41ec1be12d4b0e8b259c66dc5c28b5dd2ed5a796504a856913fe6736`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.7.2
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
WORKDIR /etc/varnish
# Mon, 25 Aug 2025 17:58:49 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 25 Aug 2025 17:58:49 GMT
USER varnish
# Mon, 25 Aug 2025 17:58:49 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 25 Aug 2025 17:58:49 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe451e59d5a26d09a97e3b79e0fb7928afddf267c3a4ace7572b983111bf8d6`  
		Last Modified: Mon, 25 Aug 2025 20:20:28 GMT  
		Size: 83.2 MB (83185485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7669faa581f84cebbcac15660aefb9984eadaea3a34907d33cded10b27e1a`  
		Last Modified: Mon, 25 Aug 2025 20:20:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a64527dd154f2a9eba53298de58121c0b9fcbf587db033481f014b7ce12389f`  
		Last Modified: Mon, 25 Aug 2025 20:20:19 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:146673585c3d37024813e5e86b1550f8db3ee2b1b1e68d60b61deaf10c74ab52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbfa2aa47df4d86c2bedad50866c1fc6026b3476d5e7976d94317120de2f256`

```dockerfile
```

-	Layers:
	-	`sha256:9d590b301fb8ee1aca3ea356538906e1103fcc95221d21906cbc6df767c7a85c`  
		Last Modified: Mon, 25 Aug 2025 21:19:34 GMT  
		Size: 19.6 KB (19616 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:f977bcbfce59e3c3fb4fa8fc51d9201928aeaf234d2a6923d2f01f679b243164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111784124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eef075003ac931ca993c4d20d48e31ff793602eeddb8fb87c40c74cfcfa39b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.7.2
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
WORKDIR /etc/varnish
# Mon, 25 Aug 2025 17:58:49 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 25 Aug 2025 17:58:49 GMT
USER varnish
# Mon, 25 Aug 2025 17:58:49 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 25 Aug 2025 17:58:49 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56553a8c424aca796da210e706d364a815b8005c07cc8f191fd94e11d5a6d099`  
		Last Modified: Mon, 25 Aug 2025 21:19:23 GMT  
		Size: 78.2 MB (78187862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd22736f2770ed793507366f719da2c6a6d703939beb0c693798f332d38b5cd`  
		Last Modified: Mon, 25 Aug 2025 21:19:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42709bc0d7add93a37332ed9eb6b8489eb6dcf8906afd78fea612bc02737a448`  
		Last Modified: Mon, 25 Aug 2025 21:19:14 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:58889f8691c6404de9e114109cb1ac97160d982361cf6377b274992e877167e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebed44358e3854a5cf16420b1d099adc56709e73acf20c1ead42a6bfd4ed638a`

```dockerfile
```

-	Layers:
	-	`sha256:e83a7b843c84f538c8d0859629916a5988e06502a9c4915119897802b2c60f68`  
		Last Modified: Tue, 26 Aug 2025 00:19:37 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:f32a92c1220a1e0a603618e0537f0ac5c3bc1b248f63ffa30f99a4b3a3682a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93294134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59032b42c5a72c84de4b1befc481998247c40b6afb3692fd22d7946a16df4df6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.7.2
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
WORKDIR /etc/varnish
# Mon, 25 Aug 2025 17:58:49 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 25 Aug 2025 17:58:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 25 Aug 2025 17:58:49 GMT
USER varnish
# Mon, 25 Aug 2025 17:58:49 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 25 Aug 2025 17:58:49 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84421444b088e0d90e04e62800c0a02b22280007a7745a8177ae449dd4842362`  
		Last Modified: Mon, 25 Aug 2025 21:39:02 GMT  
		Size: 63.5 MB (63459027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d4b6f725ba87deaf0af0b175e993027371266b81d0e712442fb785742a576b`  
		Last Modified: Mon, 25 Aug 2025 21:38:57 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c2dbfe1c113c60407d3e5067b4b38345dd7ea9d901e8d339bb9962fe345f2`  
		Last Modified: Mon, 25 Aug 2025 21:38:57 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1948f802f49689b3890b7551d456ffc43555f84a151c5f94547f16535bda1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688245e22d7d6d70a98478feecb1cbeeb4188df9fcd86c1b6935dc4c0f34ed16`

```dockerfile
```

-	Layers:
	-	`sha256:de14e908ad1b5256f85fdf225503503298a7c09b12fb66c76764c16544fe1d55`  
		Last Modified: Tue, 26 Aug 2025 00:19:40 GMT  
		Size: 19.7 KB (19652 bytes)  
		MIME: application/vnd.in-toto+json
