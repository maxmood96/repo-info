## `varnish:old`

```console
$ docker pull varnish@sha256:ae7fd1f2777a5d7d30a9f09af53b53f783ef5318c3b14bf173585a79a12f6520
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

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:d0378566717739e9c75fdd35d911566ba287fbbea9211b55b965e64477710355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116169942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3204877e9270ee67e5debfb4e68d6adababc05f4110bc7f44af73d016c4d117a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.6.4
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
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
	-	`sha256:5f808b2a8c596d067a15da3541810c2e2c3abf392304041f3b9e30d02a95228d`  
		Last Modified: Mon, 25 Aug 2025 20:20:20 GMT  
		Size: 86.4 MB (86394613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fef5274b29475a5df3ba9c7deddf6bc9dfaabd430f67a642312ae2f70eaab1`  
		Last Modified: Mon, 25 Aug 2025 20:20:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5824c888a69c7477563d644142ea975d07bf2bfc3701cd804c312ce6a3a86136`  
		Last Modified: Mon, 25 Aug 2025 20:20:12 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:3ce92534e1ec917e72fcb971730f4917ca98d622aac606e1f53b6fdbac5fd1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a9c78016fecd1e8b186841637bd4126e9580cc5c2dac5444677c28519ffdb`

```dockerfile
```

-	Layers:
	-	`sha256:f720d313d384ea00dc13fda0327c6b73488ae995fa452fc02421aa3e467ade7e`  
		Last Modified: Mon, 25 Aug 2025 21:19:34 GMT  
		Size: 19.1 KB (19067 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e968a4f73133742b613298afbb216923b7934829eff10b914f077a42a433d917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82189852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237d3a3fa88c3b5da19760d46401830b3dd6c495371d810202acde2fa38f5d0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 22:43:35 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VARNISH_VERSION=7.6.4
# Mon, 18 Aug 2025 22:43:35 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 18 Aug 2025 22:43:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 18 Aug 2025 22:43:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 18 Aug 2025 22:43:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 18 Aug 2025 22:43:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 18 Aug 2025 22:43:35 GMT
ENV VSM_NOPID=1
# Mon, 18 Aug 2025 22:43:35 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
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
	-	`sha256:f398fc767ad0e3f612431d099d0aac5a3402642927dce8a9031b247c5a225c66`  
		Last Modified: Mon, 18 Aug 2025 23:15:17 GMT  
		Size: 58.2 MB (58248878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2647396426022123650b5d115e0953159c18e54fc8720bac5d0c26708e58446`  
		Last Modified: Mon, 18 Aug 2025 23:15:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377d446d003eb32fee3a0b802c5f15cbe96fc3bf8b0c9d615fb8f612f9f98e8`  
		Last Modified: Mon, 18 Aug 2025 23:15:10 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:2ee132d5e6e7ad48c4dda53aebc836df64b32d08c9043ce2b93d590d6f5c6192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802b31667b959f3b544d01180f9bc664436562681811d2ca2d6b64374ef3ef10`

```dockerfile
```

-	Layers:
	-	`sha256:2e7da99f1892d3ac5e71d844280a6cd9b337e5fd982b6840a443db30f67532e6`  
		Last Modified: Tue, 19 Aug 2025 00:20:01 GMT  
		Size: 19.0 KB (18959 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:250a179bb7ba48ebafdae11378b7964886e7313295449b07717dc3827ecedd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110349586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da5984285dac4a5f90af59d9a78286fd1bd98faa21ac398172ba44310772265`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.6.4
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
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
	-	`sha256:33e4983d36a634c596ff5ed673e90784fcd79d64c5c83c1aa53cebcabfe8bdef`  
		Last Modified: Mon, 25 Aug 2025 21:20:57 GMT  
		Size: 80.2 MB (80211494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ced78ad544dcfcfe193590b6d2d148a78953b838c121f953916865cef16ca3`  
		Last Modified: Mon, 25 Aug 2025 21:20:50 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0493c7cefbc08c4fd0be846d2439c29683bcda737b780a619fe0b100f447fd`  
		Last Modified: Mon, 25 Aug 2025 21:20:51 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e1dc76170ca2b7f3b5a9d52d10c82db576f703d2ffd54354c86e810ae716286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccee6544f6de4a939490bce2b75cde8c53a0c0ee039f82ce2ea517a9ef8ecc7e`

```dockerfile
```

-	Layers:
	-	`sha256:c7c18d4e6b8057feb85025c2be632ed7993bde46c8229b53856e39bbe7fad6f8`  
		Last Modified: Tue, 26 Aug 2025 00:19:40 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:ead65f75cdce0fa1c92e383a4535fbb8d682d544c6f1657e20148de6d4b5452e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114330165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b036476c9fc0d23226a2029c8e6a300b7c09f59654a65957dffb370dad719b8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.6.4
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
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
	-	`sha256:de8accf52fb6dcd0906d6438549458ec09677d7f34a09e1c757f624d67de48f1`  
		Last Modified: Mon, 25 Aug 2025 20:21:03 GMT  
		Size: 83.0 MB (83038743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261586c22614736457a8fa91455ad8ea71779134625582dc9717e425795be37e`  
		Last Modified: Mon, 25 Aug 2025 20:20:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775db48b306540b7e2a127e0708075bdcc4ae290cd074092850182c9b7b466a2`  
		Last Modified: Mon, 25 Aug 2025 20:20:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:0e81ffab672fe7f031405ff3b8cac284f083d72c5871f6e3eedb9855ed28614b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975000bc06a39f2bc6280a5d428ba91e8aac29646a375abea943dae287e59f24`

```dockerfile
```

-	Layers:
	-	`sha256:75cfbc59920aaeacbf715f81195fec5f16b41319a69c4ecb41dce32b23c324c3`  
		Last Modified: Mon, 25 Aug 2025 21:19:43 GMT  
		Size: 19.0 KB (19040 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:75c51fb78ec7b4891c8943e57cd9afd30597516c71b88f0cf2f8dbfa95f73d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b59a3b729d0995e9622d3edbf38a73a10291bf08ecd57c149e54b6b4e0bae71`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.6.4
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
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
	-	`sha256:0c5807a2fb541cdaf91e3e5529f9ac2b11d3a2793f1a9bda8b3a7b273ce0fc46`  
		Last Modified: Mon, 25 Aug 2025 21:25:02 GMT  
		Size: 78.0 MB (78033830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14abee0f6a55497bf48cb4c33f7f32981bd1d1c1b8e8b528fa0fbfe59facf5e1`  
		Last Modified: Mon, 25 Aug 2025 21:24:58 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f191bf193be59b4e438dda9f473304e5efeabfb6cd6d6902e2bd066daa67e7`  
		Last Modified: Mon, 25 Aug 2025 21:24:58 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:689dc2aa73f836a898ba1e896c09680926b70a5e1a0992fe770ce58397d9f279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6d22a4b0a0e3c896ee0f5790067e429f95ad3b7d91af6aeeb237391ff5f333`

```dockerfile
```

-	Layers:
	-	`sha256:3c026b0f2b9036e3d62aa49eaae94f53e334df653d285306aa283d81d4564535`  
		Last Modified: Tue, 26 Aug 2025 00:19:46 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:886868b87b68e6b517e8178ca3b98f9c825d168e59bdaf59d81d9a4444771192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93128914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943e43c4c0f0ae4152d716359d59a1a13474270c2d312fb8dbd98e1adf367b4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Mon, 25 Aug 2025 17:58:49 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_VERSION=7.6.4
# Mon, 25 Aug 2025 17:58:49 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 25 Aug 2025 17:58:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 25 Aug 2025 17:58:49 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VARNISH_SIZE=100M
# Mon, 25 Aug 2025 17:58:49 GMT
ENV VSM_NOPID=1
# Mon, 25 Aug 2025 17:58:49 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
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
	-	`sha256:4ed4454ed09a53c0b26c12e72b0a35e0d7cdbfe6f527cdd72df8eb1bbbb128b1`  
		Last Modified: Mon, 25 Aug 2025 21:42:15 GMT  
		Size: 63.3 MB (63293808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403bb501fe25078d3075e58b2120be9a63b9c0f2993c49583fdae6d21506bd0`  
		Last Modified: Mon, 25 Aug 2025 21:42:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6cca11f34aff0c1817358cecfd7a585391b9006a46a50ecdfc89b1ccab7356`  
		Last Modified: Mon, 25 Aug 2025 21:42:09 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:2656009cbf745e7ddab848d488326269d56efdb270fe572aad7fdd1f15d7cc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad0fa4c64ac08ba354bc346f7762055e243d4e2b8f02896a179e2214d54ca28`

```dockerfile
```

-	Layers:
	-	`sha256:37e55c8e998d09f19bdc38348bb2935087a10b117a5e96b70f557275df799d39`  
		Last Modified: Tue, 26 Aug 2025 00:19:49 GMT  
		Size: 19.1 KB (19068 bytes)  
		MIME: application/vnd.in-toto+json
