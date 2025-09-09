## `varnish:fresh`

```console
$ docker pull varnish@sha256:b0ede7c516303f4ccafbfc1127ff7a279264312e06b27a8965b816f762bd5ef0
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
$ docker pull varnish@sha256:6ea1906f66af6621b5be872303c27e841be3dbfeb25fad920106bcd1584972a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01e7e6b16318fcf88489ab37bf10ef98f6ab82f29cc546a4e247c7eac136c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18944dae82a25a4881028dd55772eed24b1c8be1950466b6eca61af312c365b5`  
		Last Modified: Tue, 09 Sep 2025 00:19:45 GMT  
		Size: 86.6 MB (86565292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979091d7194e04769585896205808e30477930f91bad468ad1ee0d8bd2f4dc17`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235840fec02341cf6a06d9789cc95025caf43e0fb0546f4d04f761f0a49468a3`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:eb4857110035e2485163b912e78d6c7b6571b70179390045e5c98559d6016c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977ceb09ae86ba9316aefad8d1859df715e250f91df628547048e4e1c07e32a`

```dockerfile
```

-	Layers:
	-	`sha256:4686e767536418e4a698907c2556dd03e0bec42e4c88727a281219cd60411966`  
		Last Modified: Tue, 09 Sep 2025 00:19:42 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d33d114522a19162030ba52c0d519272214d675caebf98a5ad08eb5ab940849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4857cee8b53c7c015034fa7fb713a19d124820b19bb35e190f7e6b96267c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e639359797c17456c01ec48e4af37d9baf75ee3c0948abe907c4af26067d5`  
		Last Modified: Tue, 09 Sep 2025 00:20:08 GMT  
		Size: 60.9 MB (60937990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180e014771bbced72cbad616ceb8444f6d848941c5d222cf2ca05114acee6bf9`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a8715837fc6167839fb47529731f895e6dc16d9c9611e536684e8b569e33e`  
		Last Modified: Mon, 08 Sep 2025 22:38:58 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:f992b2f49e938ba0f4b0b17151999161f71790a5112c46e2c9cec8015021cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97486c43c69413bd0cfb916d32fea08f17f534e580c717f1111f51e100a1735f`

```dockerfile
```

-	Layers:
	-	`sha256:8e91e51e2f4a23ccb610579876c56ad109ff00a4659ab6f510d1f08abdf22740`  
		Last Modified: Tue, 09 Sep 2025 00:19:46 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34cd0a30bda20160ff7ae516e04a1c3adef99857d02fdfcaf3ce813c1428842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2351cd19844ffc5080315de35144824e0864dfbe6e515900d5f1a66507e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95db52a59f557a64013c0413ad4c7fdfda02dc7d71dc4ada8359ad435f60aa`  
		Last Modified: Tue, 09 Sep 2025 00:20:13 GMT  
		Size: 80.4 MB (80380435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1221a4365e75b2f093d2849e49dcd43efab4c3fc25561ade12264e79369bf`  
		Last Modified: Mon, 08 Sep 2025 22:24:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac397b371684df07816dd8ccffd8a1d93cd6f2c5551537f329f0b0ab7a40c98`  
		Last Modified: Mon, 08 Sep 2025 22:24:17 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:3fcb990fe9d285b0d6e1511655fd18dd6ada705278900042a7e02128a3d4eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a283bec0356ac4ed751735e36c07ec10c1770c95c332fea24d9fc7ccc81e`

```dockerfile
```

-	Layers:
	-	`sha256:2eef8bd9e2934552fb4337fca4fba8742b2153e1cd79bb4aa0114d701f1ba32d`  
		Last Modified: Tue, 09 Sep 2025 00:19:49 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:02c9234acad0eb04a624acb34e1a426dbea290ee3784b86c78b474c36781aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114475602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e1d673a9da90136affd095c1aed23ac4ad6dafe10cd762077e5b353f526e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954a711fdaa9e018a9a6874f258e53d4d982956e83088cd21bdf4838a7c5d81`  
		Last Modified: Mon, 08 Sep 2025 21:25:11 GMT  
		Size: 83.2 MB (83183774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412dfbccb4add8bf8ea9f87514c792eb1cd1ead4780eaa7674e205104cb5d88e`  
		Last Modified: Mon, 08 Sep 2025 22:11:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eb893a0fae71e2e1992c018c0746b293311942cded5755793b9688ddac647`  
		Last Modified: Mon, 08 Sep 2025 22:11:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:79202697d68cbb52332eb571c5f3c6b5807332c4f725188a41005ad0ee7ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f8665dfd530dd16dd6372f423c0935d0a2f57da7ea6e15f046d3126312e61`

```dockerfile
```

-	Layers:
	-	`sha256:1dd9b3af765c1a491122bf4c7a2cfc1509071e35560a190211e441360dbe3124`  
		Last Modified: Tue, 09 Sep 2025 00:19:52 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb93b07d38aa9c60ef29f22da422d0bf4db0ab2a36fb584e15da11e2fc855b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cc1ecc30191b0e4f6019dd9e57152f7ceeb6cef146cd1f71f6912df8fe2a41`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeaa7de33323e9da003d76c1a5cc0bb86f35d215429e0d9f20b652378d97952`  
		Last Modified: Fri, 29 Aug 2025 19:00:08 GMT  
		Size: 78.2 MB (78189327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e630fc6d39e8589329e37f5a61e56e9ebfc7eeca0d40411c39bcc2bfccaae5e`  
		Last Modified: Fri, 29 Aug 2025 18:59:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad6337d770f926d12752f7f661984d17f9c36353f6a8ebb231a5ad950de3b`  
		Last Modified: Fri, 29 Aug 2025 18:59:58 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:6533ac132bd0b294ecfc3638cc8b04c2ab50ca74d45046cfffa7d442aefd5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad9d848ff9f848e7dee20ff109298b8e870674df25d11405b571e816436923`

```dockerfile
```

-	Layers:
	-	`sha256:2de9a81e8b94b8729ba0c57f208af387d8dc241d788317f3097bf40bd0628bec`  
		Last Modified: Fri, 29 Aug 2025 21:19:48 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:316e16056f396da312924e65681e867878b12ffbd091bec4b8bfbdcab3d2e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644c7b17565ef9c3c605d4da40e1fde193cbb69da7fe5eec550f1ccc75788f0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1660409013e5bbfdf7e7587ce45ef14ffbe6f4f1ddf9e2334a36aa2db6abc0e`  
		Last Modified: Fri, 29 Aug 2025 18:59:41 GMT  
		Size: 63.5 MB (63458571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075bbb82d37082573ab3e19d8791666edde05284ddf8f73f45bde1f03eed1d9`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e60bd286912e7a79cfb7dc558aef4ee7e621471a31ad8194f8e80357adc97`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:99ce5f6dcbc57b14b71f0a9f3990b5f6a78c7e76cb46fa68e49feab34553fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd53bd2f0c8cf8cb92f86f286a45d39252faa5929bae160e1e0e5bfdc3e0021`

```dockerfile
```

-	Layers:
	-	`sha256:b4508a75879abdd43a4e164b930d4eb6ab29efba0488ae7ed5c37f3bc5c2afb5`  
		Last Modified: Fri, 29 Aug 2025 21:19:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json
