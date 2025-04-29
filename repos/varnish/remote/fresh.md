## `varnish:fresh`

```console
$ docker pull varnish@sha256:dd39ce8dba24461a72334d1574f8395fabbb0ac552a688a9793897b38b72bc0e
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
$ docker pull varnish@sha256:5e582fe889ca8310d2438bbd359daab57ca51b822852380c213c6b757ce95d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134415217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d742f05731972fee8d565fd85b4063c391bd1a581ce6f5fac464be67f98619`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b4e8561448447b5f17cdf10d16890983d981514d3e05b75afd403b4996105`  
		Last Modified: Mon, 28 Apr 2025 21:57:18 GMT  
		Size: 106.2 MB (106185535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb22ecd6cb33ac30f613868cf419ec33d9f59a3c8730f4ce33ffaf8c3bf64ee`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c65497a18778874aa28bee2837df9e19da913bf21ba619d9a0e9cf2fc53b5`  
		Last Modified: Mon, 28 Apr 2025 21:57:17 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b4d10289b86494a80849156633f8e20e092f09cc5390c4d270f0f94c0e574366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b937ebe837f9e47fd72b397157665e81c31d53a1341960b83dbf77c8b73ba8`

```dockerfile
```

-	Layers:
	-	`sha256:af5ca19bbc966bd6ae113c6fb062c2fc3ae349ae26d039823d1d2145154f260c`  
		Last Modified: Mon, 28 Apr 2025 21:57:16 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6a100e41fb46eef46da2e74869be61fddb8e2be979a15b938707ff359626eb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104770249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f04a7b5375384cf6a2cf76912b0c3e6091577757377a9a73369bdfbae1aa35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a2973a11969224e235c7a19609c30856564510f377308e37c302400265a4b7`  
		Last Modified: Tue, 08 Apr 2025 07:32:00 GMT  
		Size: 80.8 MB (80830337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1713dc7b08bb9cdd60e561328e6bd16e9d97bf33a18521c7dcf1a8de32f490f3`  
		Last Modified: Tue, 08 Apr 2025 07:31:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4add58169f8ffe703d66907d99b3160089e6c44407e2053d959131a240577adc`  
		Last Modified: Tue, 08 Apr 2025 07:31:57 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:d6d5bb837ad1f5e05608bac229760a359fbfde0ee20d77c08d5856e2e523c2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288d976764cd4f24ad6cf9662993259acfb1e48e9e0d56746185c45cd8989af`

```dockerfile
```

-	Layers:
	-	`sha256:176e31b3823b8caaa6d4f08051beb332734e166f9048336d4a112b5b0c7797ef`  
		Last Modified: Tue, 08 Apr 2025 07:31:57 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7433f0208aaa0145a423373c2a790999a7cb56706f0cbe3a2359f216a6241747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128717884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79eaeab4f0c25099c893c0ef7884ab2ad95d6c4357878891652ac6762d49d69`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d8add19318a6ad7c3fc9f8b708eb795d4a181265f53725c482777d4bf0fefc`  
		Last Modified: Tue, 08 Apr 2025 05:57:54 GMT  
		Size: 100.6 MB (100649518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536ac9ddb2e8df4f7372f94756b9bfa60f365fb01aecfa4e828ba2399d5da7d0`  
		Last Modified: Tue, 08 Apr 2025 05:57:50 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fa254c95b9d2476f0525c41829b1f24404cb17d427324c8e0b73dbdd1ea79f`  
		Last Modified: Tue, 08 Apr 2025 05:57:51 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:8ab282ff4afa335e87419c1760784fe3e6d523cebd3438c9796f3394e37f0d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486ec3bdfeb31779000639844cac289b98f757055ec6355ebda2475382bee71d`

```dockerfile
```

-	Layers:
	-	`sha256:ac9db15c9f99056cf946eccee16e320635013ed54040f541589405ff245afdce`  
		Last Modified: Tue, 08 Apr 2025 05:57:51 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:12e085143d06fd1f852cc6e44ca2fcfc92a2c1c3ff25edb7b26bcb022e89f567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131508706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44bd4d23a67aa97268702362f0f8e033489d29f2b889668c4e6cfd6cac30b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Thu, 20 Mar 2025 20:29:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b0acd2647e8753d66ff4f8e9283a0e95cbd8d1b4a074e3587232c2c84fe5`  
		Last Modified: Mon, 28 Apr 2025 21:55:26 GMT  
		Size: 102.3 MB (102295800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693aef1f511398eb6ddf46822cf63cfbff6525e42d286ef7709c4eff63d9f45`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901bd6790d92b32002940e613c07c22254557b4a9986d92deda977a97eee74b`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b5a68cfe963088ffd67f5e2047080feb3e01c5d362ed65d6a2af9a381cdb043a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1f91bec453456dd78729905045a12be8b3e823090abd36546cc3bbdad60a4`

```dockerfile
```

-	Layers:
	-	`sha256:c6c6cd5add8cac6fe641c8ebd9e866072721b41e52effcfad7b52262602f33a1`  
		Last Modified: Mon, 28 Apr 2025 21:55:23 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; s390x

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

### `varnish:fresh` - unknown; unknown

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
