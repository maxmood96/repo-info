## `varnish:latest`

```console
$ docker pull varnish@sha256:37668a82d3534e4b3b2c9c68bf72de9e37b8fa234a9f4acb2f841840d75d0156
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
$ docker pull varnish@sha256:53efe1dd2d1337d15c1f3d1e830f67d5c01e4637f9a7dd37f0200cdc0036c240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134417358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0358a26402008f34e52c2a0a7492832d938313897b1566a755c30b204e7c19`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaf4b293bdccb68f098c8fc4fe371cb8205cdaa0c2ecb511886732b6a7fba82`  
		Last Modified: Tue, 08 Apr 2025 01:26:27 GMT  
		Size: 106.2 MB (106188050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc5abf46d44dd9c3246cc3d70ee5bf53965c5be2b6da289200c74e9d219568f`  
		Last Modified: Tue, 08 Apr 2025 01:26:24 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2780559f03e82a4d13e7d8c7f7da8152ea59b21f33a65dde7a89f4b2c6ee4a74`  
		Last Modified: Tue, 08 Apr 2025 01:26:24 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:ec70ce6b3227c9545a0af900aa6675f7e2450b553416fd354d0df0e95da227bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39c29070723cac334dba5c2a2e63dcc1cbb04f52015c343afb573c4b3507b59`

```dockerfile
```

-	Layers:
	-	`sha256:e7e4932094c5e9f66d05fdae0c2844548de0bd1c2429a0107ae03936a8aea470`  
		Last Modified: Tue, 08 Apr 2025 01:26:24 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:71e3c70242ab456d2a50d1852fdf1bf22881a60214d5f05718d38bc787e8b043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104746899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5471626fd1587e61fba0fd1536bf18ef5a3f8ffb5771dbaf8b083c40f005a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ad3549916967c8bc0211f22d2e7dd7ec6928aa03fab7f5a0c11d73144a443a`  
		Last Modified: Thu, 20 Mar 2025 20:49:50 GMT  
		Size: 80.8 MB (80829766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca7549b015b88d28f436fca188518f2e2d2f3648557eec46a3d3fd6a264da4d`  
		Last Modified: Thu, 20 Mar 2025 20:49:46 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1465bb6138678775ba71c9e378c15b3fbb84a038bcc9a704d7e83c2d9c839dfe`  
		Last Modified: Thu, 20 Mar 2025 20:49:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:dc910d7f701d2a02ea2eb0c9e16d1eacfb577c235ef5cc166352714c04733547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f3d6808a7394d6b30f850db598ab37c575d1c169d762d38aba2399d311abc3`

```dockerfile
```

-	Layers:
	-	`sha256:0d69e77a1fe867bab22459d0caaabaa8162530e268c675ba5f1190bece191127`  
		Last Modified: Thu, 20 Mar 2025 20:49:46 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0813a097ca4c2835f19a5072693ce3c76c7dfd3b6dd688f0cb0594ef31747fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128695544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a350e26aca91e45f5a69fc64c5c891f4fe5589cd02863ddf6c95c0606bd6ba82`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c49a10620a69ffd2103a17476e6c3695084f0d8fa65c279d0f8a879dcc093e`  
		Last Modified: Thu, 20 Mar 2025 20:49:33 GMT  
		Size: 100.6 MB (100649463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3154257d2760e286523d54287b18022c978ce7e83fd678af9af35e9e1a5b1147`  
		Last Modified: Thu, 20 Mar 2025 20:49:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee24ad4f58211e0c31cb1b8de9f9d7cbfc0f655e782d5c4ceff4c9da7ee59399`  
		Last Modified: Thu, 20 Mar 2025 20:49:30 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:7263d43a5658916dcbb12bfe5cdeca68b9bf71ba746b23448200105a4d365ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f88ce4966b3018393b53082555f7ec9b9f9691dadb6fe232c62faa6f932bd6d`

```dockerfile
```

-	Layers:
	-	`sha256:b8369fbaec90c2e7b2b8c42bd7182932c75aa8d275a1127b9a1d8c8bf6d1ba67`  
		Last Modified: Thu, 20 Mar 2025 20:49:30 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:93e388d6c37a1b9fadce999de587aa7a441c8b02b07b9899833586420a0a9916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131516331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393ce9d2fc3c7429ef7942f866a24aaa0be7facf291224d527cf828558676f1a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba23439d918217ca13a113cdbdb142a031be965edc478b06ab0a5a0245ea3ba`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 102.3 MB (102303554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4215932d32969da5b491aef33571b53b303675c6cf581d80bb7f8ec3cb5b7`  
		Last Modified: Tue, 08 Apr 2025 01:26:02 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cff34b220f51a07bfb49326f0e2d86f18b9af53e3ebd081e6f9643df17c708f`  
		Last Modified: Tue, 08 Apr 2025 01:26:02 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:4b6428fbf5400a43a474ddabe68d721b2f2e3fc9106ab9691e2c90f4631826e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3da4a2f8e557f361c9257a4caf0d0a370e45b9d2e2c3e6acf71010b959a008`

```dockerfile
```

-	Layers:
	-	`sha256:f9b37e1a5936d8ff8dace815ebb785b13ff99612760b395faeb2d4a749ace748`  
		Last Modified: Tue, 08 Apr 2025 01:26:02 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:330ac0202eaa80f8e3e42ab0c0eea0b45e7d80f019f27669fecb860c53ff2bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137194452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ddcbb1b65c8748201fb62426bbabe5c23b07ff8d5dbcc0be47b4eb6010a8e3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84d9325c6d3c47e935b6f7511b6a9ea809b233175d9508342eee85e9ce432b8`  
		Last Modified: Tue, 08 Apr 2025 04:18:51 GMT  
		Size: 105.1 MB (105124173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa19c2eef24f5e3ab8bf9eb527715d44e5d9ecedec21f87946ea4bff8b9524`  
		Last Modified: Tue, 08 Apr 2025 04:18:26 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76e5af357110c2171394fd46026472df1d634454bb20a13a4738fcec24c4a4b`  
		Last Modified: Tue, 08 Apr 2025 04:18:26 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:606374ee04582508207681f555e7b6715bc6cea7c9e62ee164044433cf98d541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4514e3730f3ac50129bd5a07fcd29f5b9da7eab698705343c9348a643b70d714`

```dockerfile
```

-	Layers:
	-	`sha256:de3877f041d4110a70dcf352b0158847f82cf6a6ce13216167e91a87d06c38d5`  
		Last Modified: Tue, 08 Apr 2025 04:18:26 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:dd52f2e202e48f1ed1099cc7c168868f56c07b48beba85fa46095419c24c25ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112318005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b5d91f7c4da6c747b38a2fa5c7e4d7eb483aca9a065184660c86f364ba729f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 20:29:21 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_VERSION=7.7.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 20 Mar 2025 20:29:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 20 Mar 2025 20:29:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VARNISH_SIZE=100M
# Thu, 20 Mar 2025 20:29:21 GMT
ENV VSM_NOPID=1
# Thu, 20 Mar 2025 20:29:21 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.0 DIST_SHA512=5c79cae2d20dfe8aa82f0ee7ae40c644cbeba80f8c6506426ccc15de909d88d7a5bb01c6843c0a9ac8e8cdaf1f3b3526cea0b6bf3a15c85924a3f2f6b0d42c47 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
WORKDIR /etc/varnish
# Thu, 20 Mar 2025 20:29:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 20 Mar 2025 20:29:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 20 Mar 2025 20:29:21 GMT
USER varnish
# Thu, 20 Mar 2025 20:29:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 20 Mar 2025 20:29:21 GMT
CMD []
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c40b9fa7580793372fdc8e07a54501805312ec19105b32b1ff841b834b06f`  
		Last Modified: Tue, 08 Apr 2025 03:38:41 GMT  
		Size: 85.4 MB (85431355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912fe9a787a8c5ee9b74c1b5c74ac959055f8c29e00928b8995be641eafcaa3c`  
		Last Modified: Tue, 08 Apr 2025 03:38:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a246817d6333ffb12c920c5caee1720c649b97ee4b72c6c4e760430ecd7199`  
		Last Modified: Tue, 08 Apr 2025 03:38:40 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:e263aaf2aa3785219218dbaef108c496f83911e378ce05013d86553a638786e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588af427a6fd419f1e88c9c6799784869f14cbc210bbffd730a418e5126cc482`

```dockerfile
```

-	Layers:
	-	`sha256:8d63436c62b0eacf52536f9f4e9b568b73dfec084560399a73d7310db3327c26`  
		Last Modified: Tue, 08 Apr 2025 03:38:40 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json
