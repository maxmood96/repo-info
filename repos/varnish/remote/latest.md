## `varnish:latest`

```console
$ docker pull varnish@sha256:408dc0eba2281b00497ffabe032388680a8a975afb723af165cfa1fa5181a5dc
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
$ docker pull varnish@sha256:7ea7bcc1b3a17ae4a8ea77fa4c9785774199caa290c94f51a5a54eb7b9a4b5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110117553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f5193be62766ebf944f12c3a34cf96782feb73865b5324ab3231ab93049dd3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78229301a93b8fc43f0d696d4f55cfea46e0fcb3ce86339293e121b3b214be3`  
		Last Modified: Mon, 18 Aug 2025 23:03:01 GMT  
		Size: 81.9 MB (81885256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b93b4b4b9fb439878d48115d1aeba6b8bb64705b586ded443f91ee4280099ff`  
		Last Modified: Mon, 18 Aug 2025 23:02:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c5c73e79770da47ae902851836448fb8a612fed23f393295b469f3f7c6d028`  
		Last Modified: Mon, 18 Aug 2025 23:02:54 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:d8839037c3303ef15fd441a3bc7292dadedaf7803add53e7920a18e8bb5d702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b439b9955b7d0b7322296325976fb6a8177fdb1399065bb150d815bdd9cd66`

```dockerfile
```

-	Layers:
	-	`sha256:13f722aca4a393e967d8d945dd1b2defc57853181923cc8bd87ede0ee02bfc94`  
		Last Modified: Tue, 19 Aug 2025 00:19:39 GMT  
		Size: 19.5 KB (19476 bytes)  
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
$ docker pull varnish@sha256:04a75ede50687832fddc3e14dc91ce759befec433a6f0e355f64ab1a250af1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104629917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9fa4b523b0c473dba65facefebac9e17f4886253e9c04d66b57a1aca930ea7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92363535e546878053a606b85d500900972f4192b9b059f0f907af4e95368d7f`  
		Last Modified: Mon, 18 Aug 2025 23:02:19 GMT  
		Size: 76.5 MB (76545871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f20f4c4dea58be421a978d8b02b2e9b3513e6fbac4dd59c6aa6056ab254`  
		Last Modified: Mon, 18 Aug 2025 23:02:13 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f594d5db250ee887cff7da5dda3f8e6597539a0010cb6686b9c9ba066fdbba`  
		Last Modified: Mon, 18 Aug 2025 23:02:13 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:218ae25418baee022f3bc619064198868f5f8822124a4ffddd0f3a6d14ae8ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0c7bf95a68ae240cb5da680a14e5ada1c1137337b2b994eb9c2e4e6834ea0`

```dockerfile
```

-	Layers:
	-	`sha256:a9b853267e5d3f757ff6aa9923dc3f07c51fc38e5734e52bdcc255971f85a4e0`  
		Last Modified: Tue, 19 Aug 2025 00:19:46 GMT  
		Size: 19.6 KB (19592 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:b65a56a49e0ed610d2b099b2092ccbee1adb47dc11f79b2ca92992dd55157682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107514629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c01bc40dc59377d9bc294bb42f761f17622458ce717b78f3d72991a0e97839d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
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
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b2cdf135b599b0253d748c22cbfdb5ebaf357b8aee207c1e3ecad8704cad68`  
		Last Modified: Mon, 18 Aug 2025 23:02:43 GMT  
		Size: 78.3 MB (78299981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f87aa8422dc111b8e7442a1df53d8dbb3a54dfc593b1e22ba3f8fa49f7856`  
		Last Modified: Mon, 18 Aug 2025 23:02:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56ec2734e65468e71d61acb47459e640004a5aca65fb4e70890db36147b104b`  
		Last Modified: Mon, 18 Aug 2025 23:02:33 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:fae05b93244e57ef5f4e05aa051a7e3f5faaa1305abfa51491db7ae6797fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fc1245342d6b1171902bc9c036b0e964e0c7d2e984608277f2471c3a0fe251`

```dockerfile
```

-	Layers:
	-	`sha256:d66abd2fa1969af8b0383b74e24c7805a2c0a290db1b0e47b0ac8d5282d07cf6`  
		Last Modified: Tue, 19 Aug 2025 00:19:49 GMT  
		Size: 19.4 KB (19439 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:8fc3423ec4b0a5fdf7841bae035700df28dc5a2047bb0711b5ad6e93ced2c636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112138341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36501ab0557c5c63204b54e300a0479fe91d7ae151982fc8a4df57de35ae75af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759dad8df5de2a67204ebc8e92522796783a8c2d0c0962779b196589029c400`  
		Last Modified: Mon, 18 Aug 2025 23:04:25 GMT  
		Size: 80.1 MB (80062873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f899cd74e000ac44e705d1a2778b828a183dd65142628fa3393dbb417ad33`  
		Last Modified: Mon, 18 Aug 2025 23:04:13 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12801ed1e2643c7dbfcad652c039eee0ee2fe93a36c48688641a52200742f24c`  
		Last Modified: Mon, 18 Aug 2025 23:04:13 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:2d6344f8510e57b0dde129645240359576d6c465104835eca4fec89cc4272809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f48177c06f361c9683ccd2bbd8b150f8daaf719b962c9aafe061b4424d1ff00`

```dockerfile
```

-	Layers:
	-	`sha256:a76e2c3e4dfe19c45a5df71d5576f5b8dab26c5b135caf58a9417b53ee0307dc`  
		Last Modified: Tue, 19 Aug 2025 00:19:53 GMT  
		Size: 19.5 KB (19526 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:b722fc68a89d35fa46351e7acdb9b8fd9b1ca04dbaaa419225316d99e818c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87928427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3337cf25fc25302a9cc9e3439d2c706d4932301fd7076f72360cfd23fd2ee8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e469fb51ea5bc8da418ca3e888f745cae6f59ac95a736c9f208cec6dbd132a0`  
		Last Modified: Mon, 18 Aug 2025 23:49:43 GMT  
		Size: 61.0 MB (61038544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975efcdc72f917d071cea1c9d59b7bbcb01eef3e9c5b593e2fb32e0aef64ec4`  
		Last Modified: Mon, 18 Aug 2025 23:49:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ea6aa4f5390501e5c473d7ff256b846f68c30081d71291d2170490104db5a5`  
		Last Modified: Mon, 18 Aug 2025 23:49:34 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:93f549f2664e058a3ffde724f16261d1812e02b3a12b0327c873f42c968b9534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6e50329f2ead8e1eab3dba46eef707c3a86e058c18ec163ab1b92718cfb33`

```dockerfile
```

-	Layers:
	-	`sha256:fc9b853419fd2be0b519d54b08a66f74a82c4ec5c36f31e03963f370e57b4477`  
		Last Modified: Tue, 19 Aug 2025 00:19:57 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.in-toto+json
