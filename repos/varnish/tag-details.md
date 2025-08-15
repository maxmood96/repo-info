<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.15`](#varnish6015)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.4`](#varnish764)
-	[`varnish:7.6.4-alpine`](#varnish764-alpine)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.2`](#varnish772)
-	[`varnish:7.7.2-alpine`](#varnish772-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:508c568a36f190ac356251acbb738eff0d9e50f98753925761f01e94e2b6b824
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

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:4f205404369001e63bd78cb37c84db57e99eefc0102598dd9756ed74bd3b1d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103551015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205a2b1a1f5d3dd4eabcaf07fb315d5c006eb98f4c0dd4ecd1015901b826425a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b3030307e8a54c17da978aa122b40a64286d7dd94f9021c4dfe39d4eda81fd`  
		Last Modified: Fri, 15 Aug 2025 16:56:49 GMT  
		Size: 75.3 MB (75320004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087091d157f20b70b465cc1363850e48778034d11c403fa6c5375a6e9c7581b1`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:6a3d52c00cea8a4782380fbe188167a6a64dc4516dd0584e5905e61c69d1efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239f662812bdbe99ba31e39373a27c94bdf60c9401fb1aa40a65163bb577588`

```dockerfile
```

-	Layers:
	-	`sha256:3105daaa0e7fbce636d5e26dfde9dc7e468ea3fec101c8ced4bc8bd3647a41b8`  
		Last Modified: Fri, 15 Aug 2025 18:19:40 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:63fb769bea28f1be50113c499f024710a06c6b691dda3f845e0c6ed61ae5d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75972675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545192084d1f68c292e6676630c61b0f4a703f5f749cf7b9b9af51d90755edb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f5cdc2b29e6e9f7e366dab90d0d13fe6bb1e6936c47d9a7f28c78494b0a15`  
		Last Modified: Fri, 15 Aug 2025 17:05:40 GMT  
		Size: 52.0 MB (52032989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ad42f5a97af5a103fc53c0068a770844b25168bd89f510dd1208b539ec6d76`  
		Last Modified: Fri, 15 Aug 2025 17:05:34 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:250fd3b0d47cfd437f00fefcf0895fb71dc39ae74ca9354f6952d6128f69059b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3994e63f9a6a786cab6f39a88fcc39cf68615db7197fb977a0cde17607a0d`

```dockerfile
```

-	Layers:
	-	`sha256:3f1ae9bad7cc686af951d8f0988a09bde737235f52aa1242cdedea30e424432f`  
		Last Modified: Fri, 15 Aug 2025 18:19:43 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3d8591b4c8a49bb34772636c11837f394c0427644eb1bfa5760398b302cf1f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98372375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b103782bf675afb16ccb328ff82ca3fd0d13b7c41dab6166c43ed41a92e53b31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d4c5411a8a5191465e747e040f148e3e2954ffe4efc3b5e6df88a5197f7df9`  
		Last Modified: Fri, 15 Aug 2025 17:04:52 GMT  
		Size: 70.3 MB (70289618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c5a5db02a078d9b226d17d533ae6a4873897fb3e51fd16f5e2fec3a22de552`  
		Last Modified: Fri, 15 Aug 2025 17:04:45 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:3585cf5a7a99c879f94875ff1d9dda046ffb97aa31aad46c7e35370186653927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8a622ee63b17d5b8c7c01ad26a27c25b1c03d2eb5e4676f8d5c1a0512b2b38`

```dockerfile
```

-	Layers:
	-	`sha256:176774f0bf55f60639b47cccfa92496e9c88f4baa2bae7b2f29d35b71c9bfa13`  
		Last Modified: Fri, 15 Aug 2025 18:19:46 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:c1e45daaad2256afb1d92957408e28157149055d2890299abbd06dd7eac9a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc42e044e9794a4e6b353970c333eb95173dbd6deb7983e4496934994375dbea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6c5110dee275f4bdc6a6440f5c4605e685665d32fdc0d9eac6395187e92e21`  
		Last Modified: Fri, 15 Aug 2025 16:56:52 GMT  
		Size: 71.8 MB (71798834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce5ced758f20dd5e228d5b673317afd748a1673753da7c6a676eea3fc2bd7`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:cd4624282828006ad76c2c2cd6588452b66645c9688b342db848641294ab682b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba0bb4524ec66863a46f64a64abd4d1da26c235b266c8e25e21ad3325615df`

```dockerfile
```

-	Layers:
	-	`sha256:def37e74e38e4692944a7846f46cc443d74133538355871dde977f1b20a7e8ae`  
		Last Modified: Fri, 15 Aug 2025 18:19:50 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:59ca61d9c88cec3e2a850c09b44b62e9366743ac8b2a8f3f0f56fd7647549093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105453532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ececacc8625c0cf7ed467c2ea49c947f651a65b3cf6406577b361cb99d15f38f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140f2e5f7e62807eb83bf1d06d3de2b7ca8432c4a959eee34569191dc51fc57`  
		Last Modified: Fri, 15 Aug 2025 17:13:11 GMT  
		Size: 73.4 MB (73379358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6722af99a347451a061f526da91a19fcbe85026ad68115418e60c07dc9b91`  
		Last Modified: Fri, 15 Aug 2025 17:13:04 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ca5e6fa34de326f0e638ec5ceaec95fc5b12363518101a227fb8b8cd5573e688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accc1929eb0e7d44f7aead289ecbe585947c71c34aeaadbc842633279d0c6690`

```dockerfile
```

-	Layers:
	-	`sha256:87e0a9ba0d00efa32d31b56794478a0fe0c596e0d6ae8c38d130ec41e83eaf25`  
		Last Modified: Fri, 15 Aug 2025 18:19:52 GMT  
		Size: 12.7 KB (12730 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:473b70ef10a50ce071860f7c79b3ad0fd20b97ca1326c17c989973a2b1c0e1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81338348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bed7f9db4a05ae7b0f9c6a03d049967991f6796f0a734186ace7d06b82dffe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70df0ff3df5e69e08e5b4b753ab705a5f7a7ccd7f9214d5dd81f48be05c515a8`  
		Last Modified: Fri, 15 Aug 2025 17:07:05 GMT  
		Size: 54.4 MB (54449756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe0f8eb19dd0db4199e2a97ba899a4da6e3274dcc34d2e879c85315f9d22924`  
		Last Modified: Fri, 15 Aug 2025 17:07:02 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:9af53eafac86b7f6351134d69f526deb3163438739a1bd002b592275ac7a7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d666bc79cbdbe8e4256f9ce8af8739b6e5a406e78e33a4835d3e75471e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f5be1a6ced377aa9370dc51363ceba74a5599b107c3b84abe75dc345be4f83c5`  
		Last Modified: Fri, 15 Aug 2025 18:19:55 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.15`

```console
$ docker pull varnish@sha256:508c568a36f190ac356251acbb738eff0d9e50f98753925761f01e94e2b6b824
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

### `varnish:6.0.15` - linux; amd64

```console
$ docker pull varnish@sha256:4f205404369001e63bd78cb37c84db57e99eefc0102598dd9756ed74bd3b1d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103551015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205a2b1a1f5d3dd4eabcaf07fb315d5c006eb98f4c0dd4ecd1015901b826425a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b3030307e8a54c17da978aa122b40a64286d7dd94f9021c4dfe39d4eda81fd`  
		Last Modified: Fri, 15 Aug 2025 16:56:49 GMT  
		Size: 75.3 MB (75320004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087091d157f20b70b465cc1363850e48778034d11c403fa6c5375a6e9c7581b1`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.15` - unknown; unknown

```console
$ docker pull varnish@sha256:6a3d52c00cea8a4782380fbe188167a6a64dc4516dd0584e5905e61c69d1efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239f662812bdbe99ba31e39373a27c94bdf60c9401fb1aa40a65163bb577588`

```dockerfile
```

-	Layers:
	-	`sha256:3105daaa0e7fbce636d5e26dfde9dc7e468ea3fec101c8ced4bc8bd3647a41b8`  
		Last Modified: Fri, 15 Aug 2025 18:19:40 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.15` - linux; arm variant v7

```console
$ docker pull varnish@sha256:63fb769bea28f1be50113c499f024710a06c6b691dda3f845e0c6ed61ae5d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75972675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545192084d1f68c292e6676630c61b0f4a703f5f749cf7b9b9af51d90755edb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f5cdc2b29e6e9f7e366dab90d0d13fe6bb1e6936c47d9a7f28c78494b0a15`  
		Last Modified: Fri, 15 Aug 2025 17:05:40 GMT  
		Size: 52.0 MB (52032989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ad42f5a97af5a103fc53c0068a770844b25168bd89f510dd1208b539ec6d76`  
		Last Modified: Fri, 15 Aug 2025 17:05:34 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.15` - unknown; unknown

```console
$ docker pull varnish@sha256:250fd3b0d47cfd437f00fefcf0895fb71dc39ae74ca9354f6952d6128f69059b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3994e63f9a6a786cab6f39a88fcc39cf68615db7197fb977a0cde17607a0d`

```dockerfile
```

-	Layers:
	-	`sha256:3f1ae9bad7cc686af951d8f0988a09bde737235f52aa1242cdedea30e424432f`  
		Last Modified: Fri, 15 Aug 2025 18:19:43 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.15` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3d8591b4c8a49bb34772636c11837f394c0427644eb1bfa5760398b302cf1f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98372375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b103782bf675afb16ccb328ff82ca3fd0d13b7c41dab6166c43ed41a92e53b31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d4c5411a8a5191465e747e040f148e3e2954ffe4efc3b5e6df88a5197f7df9`  
		Last Modified: Fri, 15 Aug 2025 17:04:52 GMT  
		Size: 70.3 MB (70289618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c5a5db02a078d9b226d17d533ae6a4873897fb3e51fd16f5e2fec3a22de552`  
		Last Modified: Fri, 15 Aug 2025 17:04:45 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.15` - unknown; unknown

```console
$ docker pull varnish@sha256:3585cf5a7a99c879f94875ff1d9dda046ffb97aa31aad46c7e35370186653927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8a622ee63b17d5b8c7c01ad26a27c25b1c03d2eb5e4676f8d5c1a0512b2b38`

```dockerfile
```

-	Layers:
	-	`sha256:176774f0bf55f60639b47cccfa92496e9c88f4baa2bae7b2f29d35b71c9bfa13`  
		Last Modified: Fri, 15 Aug 2025 18:19:46 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.15` - linux; 386

```console
$ docker pull varnish@sha256:c1e45daaad2256afb1d92957408e28157149055d2890299abbd06dd7eac9a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc42e044e9794a4e6b353970c333eb95173dbd6deb7983e4496934994375dbea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6c5110dee275f4bdc6a6440f5c4605e685665d32fdc0d9eac6395187e92e21`  
		Last Modified: Fri, 15 Aug 2025 16:56:52 GMT  
		Size: 71.8 MB (71798834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce5ced758f20dd5e228d5b673317afd748a1673753da7c6a676eea3fc2bd7`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.15` - unknown; unknown

```console
$ docker pull varnish@sha256:cd4624282828006ad76c2c2cd6588452b66645c9688b342db848641294ab682b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba0bb4524ec66863a46f64a64abd4d1da26c235b266c8e25e21ad3325615df`

```dockerfile
```

-	Layers:
	-	`sha256:def37e74e38e4692944a7846f46cc443d74133538355871dde977f1b20a7e8ae`  
		Last Modified: Fri, 15 Aug 2025 18:19:50 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.15` - linux; ppc64le

```console
$ docker pull varnish@sha256:59ca61d9c88cec3e2a850c09b44b62e9366743ac8b2a8f3f0f56fd7647549093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105453532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ececacc8625c0cf7ed467c2ea49c947f651a65b3cf6406577b361cb99d15f38f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140f2e5f7e62807eb83bf1d06d3de2b7ca8432c4a959eee34569191dc51fc57`  
		Last Modified: Fri, 15 Aug 2025 17:13:11 GMT  
		Size: 73.4 MB (73379358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6722af99a347451a061f526da91a19fcbe85026ad68115418e60c07dc9b91`  
		Last Modified: Fri, 15 Aug 2025 17:13:04 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.15` - unknown; unknown

```console
$ docker pull varnish@sha256:ca5e6fa34de326f0e638ec5ceaec95fc5b12363518101a227fb8b8cd5573e688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accc1929eb0e7d44f7aead289ecbe585947c71c34aeaadbc842633279d0c6690`

```dockerfile
```

-	Layers:
	-	`sha256:87e0a9ba0d00efa32d31b56794478a0fe0c596e0d6ae8c38d130ec41e83eaf25`  
		Last Modified: Fri, 15 Aug 2025 18:19:52 GMT  
		Size: 12.7 KB (12730 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.15` - linux; s390x

```console
$ docker pull varnish@sha256:473b70ef10a50ce071860f7c79b3ad0fd20b97ca1326c17c989973a2b1c0e1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81338348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bed7f9db4a05ae7b0f9c6a03d049967991f6796f0a734186ace7d06b82dffe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70df0ff3df5e69e08e5b4b753ab705a5f7a7ccd7f9214d5dd81f48be05c515a8`  
		Last Modified: Fri, 15 Aug 2025 17:07:05 GMT  
		Size: 54.4 MB (54449756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe0f8eb19dd0db4199e2a97ba899a4da6e3274dcc34d2e879c85315f9d22924`  
		Last Modified: Fri, 15 Aug 2025 17:07:02 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.15` - unknown; unknown

```console
$ docker pull varnish@sha256:9af53eafac86b7f6351134d69f526deb3163438739a1bd002b592275ac7a7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d666bc79cbdbe8e4256f9ce8af8739b6e5a406e78e33a4835d3e75471e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f5be1a6ced377aa9370dc51363ceba74a5599b107c3b84abe75dc345be4f83c5`  
		Last Modified: Fri, 15 Aug 2025 18:19:55 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:83ca6fecb7781cf39d4489bad0d357d20a8edb943f5563b90ff46d94360f4ff2
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

### `varnish:7` - linux; amd64

```console
$ docker pull varnish@sha256:fedfa20758d2651daf48ce3ae0c252539ec834fb1d8371335b8f13538c3d00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110106279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f281d5b0ed5e1cde6a33baf7c1a3f71055bd16d781940ec42a1a6be11bca5144`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767674a186da8285836153cb726409d4112a4a80fc976127bdf22c5df07a342`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 81.9 MB (81873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a35607832b0b15801f55356a07a24586b93213ef9a8d0c65fddc881463143`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddb218959aa0785586687d3d0aec6ce87943c57d054025007ae3f5f5780c5e`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:0e470651a8e0394799e7bbdf63d667730f87b8031f5db0a6d6dcfcc9aab04caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9b00d45d0fad1c56cab3e0d94f609b0838c8cd95edbd9e43910024dab3c76`

```dockerfile
```

-	Layers:
	-	`sha256:093b8a36638c67c6ebd86a569d5a9e880125463b6121e13cb842711c247e53df`  
		Last Modified: Fri, 15 Aug 2025 18:20:01 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6ef60b34629736d2141c8fb33ab6c2ea3a6a24b49a8cd2734b5c616daf0b8ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82361579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65f47712081b446c96886e6775c5643a2e8b77b1f93bafdc4d9060c488ae3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865acd02bf9c4f607ff081eacbcc80167f492e47029b6f33665a0092132885a`  
		Last Modified: Fri, 15 Aug 2025 16:57:09 GMT  
		Size: 58.4 MB (58420605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a9cb9947510c533811bb4f8ea48b8875ecdfcd746a0059cfb266744b2edb6`  
		Last Modified: Fri, 15 Aug 2025 16:57:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829b90f4f1f7509e840ecadd5046ff17ad077e9fffa3d6045fdd90d2b67b3ec`  
		Last Modified: Fri, 15 Aug 2025 16:57:05 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:5a95c4e9bdbda53ac19a4f7eb2fc7871c27bc54ec62f465520f9fed03f72c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ad9b4ae87f0700a77508ce6db54194c580d23dd71847fd987a3c2785c4571`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcf08c3380eaf1388cd59017438b8bfecd643cca66768e2856226c4b8100ce`  
		Last Modified: Fri, 15 Aug 2025 18:20:04 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c022a0ff5f7d30d8d65cdd3aad6a97f02e4d2bf8b551977c74d3e6784a78db30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9ba230852531c6b2deb4e5aebc846e12855d713a6f1daadb2367d71cd98992`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121caf58da77aa0443a2496d57c85ea79d8e1df2405a26b8d5e3673b479bf20`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 76.5 MB (76538135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec5280a3b9e492d66687c59a64df4f0f155ba5207db69037007ae5fde08120`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37110db52b9ecad7c7a879bb96852fe0ef35b0ece8dd3887a49bec4d0dfc3f3b`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:751a4801d5a9c5f699faad34be2f5905b06088ed10bf52f8b0b80ca728645a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664d38510adf7bbc0020d7dca45643c6126b6c65e459171cc4d00fe610eb1d2`

```dockerfile
```

-	Layers:
	-	`sha256:cf2d904d3d707278b34f5a4903707327e72e00baf0ae5df1a13efedb5d611426`  
		Last Modified: Fri, 15 Aug 2025 18:20:08 GMT  
		Size: 19.6 KB (19572 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:643e67a2f50b57bca50e83839f7f8b91b3c47588dd396769ede34e6db05e44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107508252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db414121d0e199a39b26554aef75af674c08942370d3c88386de0e1d008c1572`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a29dc117e0a7cf8a15e635b05ccf4d12c7a1ee6067cf3f182e71f264226655`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 78.3 MB (78293602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d90c530a68e0fbb406e32d98113522350b1170c276aaa0c300ec0cd5d34471`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020470a039d54dd250c2e33a0b7ad201a5a7dde161b96dd8aa20f54f65eb06d4`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:e403282207a41140505699aa134579847e5933b7c004aed9a357a12333a68bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c959bbaebf235be5668c87882884c538a7ba91403725fa4595ae53166076fbd`

```dockerfile
```

-	Layers:
	-	`sha256:9670f5aac7a9527cbdff76983554c8c1405a95db2b3b9ce78a62e32be01562b5`  
		Last Modified: Fri, 15 Aug 2025 18:20:11 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:5d63d6d9b3a816d335ab85a7fd3c24f078e8661c94d90f82cebdb65328894de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112125451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855097713d44be414c5475db87bcaa3807ac765b8529db689eff325ef52a983`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063bcd1ca526e732f14ddda8346106790e36b532d8f7ebbd7939f1f3390c975b`  
		Last Modified: Fri, 15 Aug 2025 17:00:10 GMT  
		Size: 80.0 MB (80049983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71734c96c8bc5b7e443557665eeda472a075a5cd5a0ac09e3b768ccbda14da8`  
		Last Modified: Fri, 15 Aug 2025 17:00:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b495f9c9889d394cacb9be69d494dc4f799f756dd6b652c7771f56bb6a8f82`  
		Last Modified: Fri, 15 Aug 2025 17:00:05 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:85986ce2cb4509cb6fa45a8f3c09981811c4036abad32fb472dd68250e65163a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dffec5d24b702fc55c635da910ac3d0da72d6da380f0d1e227dc9278646f6f`

```dockerfile
```

-	Layers:
	-	`sha256:a1646d6d4130c7e1c7b72eefc76d27ca9be0ce2306db99bbe68a55856ac896c3`  
		Last Modified: Fri, 15 Aug 2025 18:20:14 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:9141e45c7cd14117b58069fd59d4cc53c8badaeade8f9a536092c8143aa8e571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87911883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45dd74ae8f7452e7c68d37c305c66ffed0cac781869788d41e4882e352c37cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead03c3e8d7cd776db98c9f94e1610ca909dddfc22e62d793c6301988e7b4a97`  
		Last Modified: Fri, 15 Aug 2025 16:58:16 GMT  
		Size: 61.0 MB (61021999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f194092d9bc42b54e915dbd444d3b36e8d1e5343277b869e660e9ca0886c2b`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beefcc26fe8cb04b79d3ce2dbfeb6e61ce0c3553afc049dcf524ae6c44a25ab`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:4ec9d06a7ed84cb2369aa6497a334a6c5f94ed608f6bf9fd1c15e714d634b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f886ac06337c55578efdad672bd8221a76bfc5292462fb8f685c13c3a755c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f619217400a1c21827da3eb8bcf12dd75b9983fdfc57d3fa43c9fa87674f776`  
		Last Modified: Fri, 15 Aug 2025 18:20:17 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:11f468c0fac3c1c019ed680d37f905a4e97cf4d87d562202ed1ed6dc3054d7c6
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

### `varnish:7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:7035c20e4805ab5f70599ef1e4057a1aa57ad7ae2d50f8409a93867f1cae4e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80505421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801bc1bb3b98d83d0802e4e829cc1218ea8134d53b4f06104d9f13978c59f0b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55297ffdb439992b8f725e1abee5cfb1f41f3c26beabd7e2bbb004029148296`  
		Last Modified: Fri, 15 Aug 2025 16:56:50 GMT  
		Size: 76.7 MB (76703672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bd86dfee1e73c6276ee94e788dc89ba827a83d22f4454a2011064fc9f82f4`  
		Last Modified: Fri, 15 Aug 2025 16:56:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539ddb67860c1bfec8f0ac73d49a345cdc44ba46ab1b6da9ef818f68cb290cc`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fff050818c236d2652dff618185a1b092aa7b86c042cf9dc46eb0c5ecc422843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb200068daf0e7aa4cc2e7d0f920c1c9b766b6f86e7ef8224f9c40022498079a`

```dockerfile
```

-	Layers:
	-	`sha256:b233189ccdc4fd3796925be1bb23d5c8269cefe12c4b7b0d123c7f36ffdf4156`  
		Last Modified: Fri, 15 Aug 2025 18:20:16 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9e81fcdb8ea18f49dac62d0e6f2395e6c5d1ebe5b537c2343ebbcdb3dd487397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62515065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9411aaf5f3dbef0e91342c29cf7d595ce30ee60f41d66e3fff2a369f4b1d8dfe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c6c5dcb5b4ac9ad073457a12700618c82623de85fb82f2d5fb326bca6a600`  
		Last Modified: Fri, 15 Aug 2025 16:59:02 GMT  
		Size: 59.3 MB (59293972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d82b3db827a281bb380ace01fc619eaa48d752c82e2fd376a28c752f1465ff5`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97cd2adc93836662f8319b7754daac32766095945bbbd68c407d62f8b7e1d98`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18353cb316e339f32e46a86e9a14cc92c68611618f1d0e7e409c14d87efa920b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fe86f4fcf0d2a0df26272c5ad8251508207e05b0fa78c65a4c02e77d0a1e9b`

```dockerfile
```

-	Layers:
	-	`sha256:eca07e957d3e688c6caee11f6b3e4e3efd6d17f0fbb83518fd0f96c10962a9e5`  
		Last Modified: Fri, 15 Aug 2025 18:20:19 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d6df66a151a86aa3c614afa6279d5bea14710a86ce3dfab839160b94d1e80ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77498564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053598a7edda72857a2903a0b0371938657afa3a81079b4cfae7a9555359b01`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34fadec23958052f927e36d3e2fa9dd9b9ce78567638099bc0d9334feb4d93`  
		Last Modified: Fri, 15 Aug 2025 16:58:43 GMT  
		Size: 73.4 MB (73365758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e96be58cc45f2ba927d34bdf0172d2b8d7377124a996d42e808fdf4cfa3b72`  
		Last Modified: Fri, 15 Aug 2025 16:58:40 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98997d85e5d6da9c6d5dbf443b23fdcf0669368bd779025a5a1aa111a07e05f`  
		Last Modified: Fri, 15 Aug 2025 16:58:41 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2561dd56ac33c571b7b332395ece35ab92caa03f3829fa1196b1c368651cdbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b4eadb528c844dd226ae97105b841aa3bdec59d3be2ebd796fec7b00c04d54`

```dockerfile
```

-	Layers:
	-	`sha256:40af3552a2a3f4340d8e17e4d4daabf005c1c861aa2e8c1c1bb700cbcaeed15d`  
		Last Modified: Fri, 15 Aug 2025 18:20:22 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9a1c3998552633081142f8c46765d5f54144dbfa64f3433e87faddf2c883d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3709c2147eee9862efa2559144884bb8f59697f031c38c5f4e2fd36d829454e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5273443b55588922d029ea0a105bcef20161f7347f7723a8a2bf00ba5409c29`  
		Last Modified: Fri, 15 Aug 2025 18:20:52 GMT  
		Size: 79.1 MB (79115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5306d254fb0902aa4460d62f07845d4308e97c4f36214af53ad59455348b0`  
		Last Modified: Fri, 15 Aug 2025 17:27:23 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd7e5a4c259b0e2da55fdcc2a951ff2d4e57059a085970ba0a2a457820011b`  
		Last Modified: Fri, 15 Aug 2025 17:27:22 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:805ac3dbf45f6e2a1dbf9817a7b6a69e3226fdb19a16bb57330437319a30c730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9395e2b144bc8f7bc98fe149d18657a2e7b81ca6069c270aa4bd292983f413c`

```dockerfile
```

-	Layers:
	-	`sha256:817b6ca8afcbee4bba4d42bd3193dce131fa0fee46f80e1ba8c59a36877f5c1c`  
		Last Modified: Fri, 15 Aug 2025 18:20:26 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:4013273c17e4d73d0fff79e87e82d992487316c0462b023c2127b71d02b30ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76633537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d930a8ffe8c5620edda4a5ae4083beca22509b76dcca3f020352b803f9fa06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace93df466c17cd7ca7913c595aa0c794ea5fbd619f8289dcc0542b678139a1`  
		Last Modified: Fri, 15 Aug 2025 17:15:37 GMT  
		Size: 72.9 MB (72904365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98130a78b774a02fd26aae942aa7184d419e13cb2f08db2862a314215672524b`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9bc2376dfa75b485a5fcf0d9ffc4339b721217e78d0301c550afd8852dd93c`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b782e164fdc8b81adc6e74b39ae3b241c8a92987d16b383bc97a03b90d718e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230eaceef94b90468bf978df0fa292d7206e25542088ae0d930c0646ae9d272`

```dockerfile
```

-	Layers:
	-	`sha256:3cf726d2f7ef3fe6dc191ab3cfc4480ee577512d43c5c480b633013e45b4c749`  
		Last Modified: Fri, 15 Aug 2025 18:20:29 GMT  
		Size: 19.5 KB (19518 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:be77e8e657b601fa610f69d3c57c0d2477b9b7114b173dde5602654fd5d0416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89093a7ecc822c5b6def0853f54aee46c86cd4eb988f9c443e962fb9f0254f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b4cd4d200db742fc36965160bffa32a4266c50fe01a3a3098c5dd0c6f6ca6`  
		Last Modified: Fri, 15 Aug 2025 17:00:11 GMT  
		Size: 67.6 MB (67637480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd6b2622d0e954a05bede36e6c5572d4003aaca0a717adbcafc33fe4b9de7f`  
		Last Modified: Fri, 15 Aug 2025 17:00:06 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671b8de9982d6140e072fc678c363fb0760ca978dcfdcd4721579178cf7402e`  
		Last Modified: Fri, 15 Aug 2025 17:00:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4d661ac5f10739ea3990846451b229f77886a428fb934502f7809c628bbe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e5a16b6b5c9085598ef0af0b1290c2dee11db9794440119a10ed5d01fcec2`

```dockerfile
```

-	Layers:
	-	`sha256:c3364ad35a3f174f668207d29078228dc7d165a94b113fdb93703a0b7fa2b1a9`  
		Last Modified: Fri, 15 Aug 2025 18:20:32 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:55ac9db07a2b148fa275604f15a9b94f26445c54e11e1701f9ffe9729616ee37
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

### `varnish:7.6` - linux; amd64

```console
$ docker pull varnish@sha256:a1fb2f20c12438ef482bf8149aece9528fdd8b24b6343ffa182a843889d7c2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109935364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a4d0525acdefa194b1cc9c28c9af7c752cc3cac711727419f40e73fa7fc387`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09267f7e5a383c22b01ad0bf5b02384b7345434b494f8a60bc90cdfb66934070`  
		Last Modified: Fri, 15 Aug 2025 16:57:49 GMT  
		Size: 81.7 MB (81703064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6f128744545326a15166b51afb3e08827e5cf2afdb7f60b6ce1208e3e95d14`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6829a15a5bc04c257c64e3468ee5f3e0b43ff44a6eab0e3d7382967f444045`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:c222ef3b761cd4101767ce05ce4b3e7c56239128bc44e89e672e855647aecfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0556654bf18f33829c58cf35fca961103727c4188d34ec864fd5202871997ec6`

```dockerfile
```

-	Layers:
	-	`sha256:49690a315c3e50f7eb6d14c4bef2ef21a322a1b4e5310dba968ac567847b216c`  
		Last Modified: Fri, 15 Aug 2025 18:20:31 GMT  
		Size: 18.9 KB (18871 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:2dde0e165d54e25b0e0a42fcd98da86647a66f3cb6b28156330959b50e764370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82185203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc70aba460a17488c1dcffa90c4ac199283b309d2c4e24f5ca0de078f1dc599b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c482092d910c7110f0605ae4db82097e5f488b42c827f8abe3baea139c9535a`  
		Last Modified: Fri, 15 Aug 2025 17:01:45 GMT  
		Size: 58.2 MB (58244224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a4c5dacace037dd116a534d3e2e6cf0061119c6b1c5418734ba783d7515ad`  
		Last Modified: Fri, 15 Aug 2025 17:01:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fd9c49bf7a0d3736d7214af56dfed1230f54a846dc3380c17540eee10dd1f2`  
		Last Modified: Fri, 15 Aug 2025 17:01:35 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:2b37a8c98eee509364d75ab8f563bde11976bfd70be7c499813659cbc2745ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617b048a15b0acca175b3a678db24692ca8cfacf6796525c717a1c4654c3f5`

```dockerfile
```

-	Layers:
	-	`sha256:6eba3dcedecd35442cb775edd859623bab177e01b7febc0e98b174e0cd568939`  
		Last Modified: Fri, 15 Aug 2025 18:20:35 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8b7c11552292d531475f0d54463beae68da5bdf7d859eb1a83a47afb479f270a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104449591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fa7fde6ec1a84fba9665510b54fdb2994fb2735d988f99e5778aa3b42bf80b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd0936b3e7a1906e0dcd9f67846122080e0fa52bd067c4fb7fc279ae847d0c`  
		Last Modified: Fri, 15 Aug 2025 17:01:23 GMT  
		Size: 76.4 MB (76365546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21739974fa1f38fd215745094ac2db46becce16d34d034a3a2c3c8e62a0987ea`  
		Last Modified: Fri, 15 Aug 2025 17:01:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c890712c0af0dc42f3c1a1a7db2493a3c986de76bea5c7ee6ead7a2911a6f43b`  
		Last Modified: Fri, 15 Aug 2025 17:01:16 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:e934bfe8943e75dbd1d6bcd8e27048c270da9c865168d9a88dbed68bf1c77328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b43d13e42577bd39579d32bbf27a9a995b8b310bb766e1358677b0c0d6688cd`

```dockerfile
```

-	Layers:
	-	`sha256:6a38d12aa59e268d53752119c2808a8922cf235d7335eaf0b0f450cd0afdfb93`  
		Last Modified: Fri, 15 Aug 2025 18:20:38 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:10a5db2b243687d760fa20c79999a7c632b4691793acc4dd1a5d95356d02db16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107339580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd50e7d7df3a4b515a1c8ae46a155d2c5bf426c62db280ca2fa8365071bca83`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c62e81843249b5cb46ac342e6453be1c2b9d3b959437306a9a077d403976b3`  
		Last Modified: Fri, 15 Aug 2025 16:57:46 GMT  
		Size: 78.1 MB (78124931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc091cc50d8ccb50f08b1eddff8c15d443ddee40df8eabcd21c594d5826f44f5`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1922589f9b12760e939f8eb0c74c48a75dcaf00c702c049b7b360aa83c15288a`  
		Last Modified: Fri, 15 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:7ee892531be69de90be55946b0a76a0c6ddc8be3a38696bf99e733b2362a0f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec6abd510c3912a99835ec879a9914911d4495ac9f7d6063b3f7a036839c6a9`

```dockerfile
```

-	Layers:
	-	`sha256:9b42f2b3d67bc1dbd8f2ba77391f5a5562ae5eaf1da2f64250db6463a0ee8589`  
		Last Modified: Fri, 15 Aug 2025 18:20:41 GMT  
		Size: 18.8 KB (18844 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:d771d0a11e5cb044fb29e243105d0fbaab24c34f772c4e6161e5e6cc6e2aae36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111970696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7fbf7aea862f1ce5f5b6743855ca732d0f26f5bf013b2bab03fd7e6a722e56`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f128671fcf877380ff6584510acfe5b88b91f2658c3348c827730b222267a31`  
		Last Modified: Fri, 15 Aug 2025 17:21:02 GMT  
		Size: 79.9 MB (79895231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981a0080d7c508255eac372f3977fbeb18600432db4ca13c65d3a567527af707`  
		Last Modified: Fri, 15 Aug 2025 17:20:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8407d8692a211522d3327eafc25ce587b9c952337fd433bb34be66bbd2517b`  
		Last Modified: Fri, 15 Aug 2025 17:20:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:479a8356add5b245a038ab07bb03f40962d410e4cff3fe671f0c3c35c7c45c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d3f1bc54dacefb5e68e75b5ccd1a117df8d285362cc6e80737b2fa1efe994d`

```dockerfile
```

-	Layers:
	-	`sha256:08ec36e5441b3a6da7a97f757f3e01f7b9a3d321e129455be42b51382a74a2fc`  
		Last Modified: Fri, 15 Aug 2025 18:20:44 GMT  
		Size: 18.9 KB (18909 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:b42f11c5699d210935309a878e399a8123e82e28ff9753c2ade5c960aa5d7080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87740299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be0ad2520373e21bff38de538ae40b78fd68435c1fdc6f4a3a7acbbb6b1932a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eb726fb2e8bff58331cf376c5c7a5e8696a9d03c548971766e4d1cbeb15097`  
		Last Modified: Fri, 15 Aug 2025 17:03:06 GMT  
		Size: 60.9 MB (60850415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b6eba540f8219227bdcc54c0371204b3f3e02094a4c5a5ab53d8970c51f0f3`  
		Last Modified: Fri, 15 Aug 2025 17:02:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac740b1ffc0d320f134e48c4c99a02b78cfb4d5948a7df22a6866d238d1acace`  
		Last Modified: Fri, 15 Aug 2025 17:02:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:50a68b601ee2b9d22d4ea3e1451db8ff2fdbf0992d3c6ed06becf9ecd3d6d75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751bfecbd724e325e691d6c1a0716f9f5d6fa5a454980a62a1e9afa46aff0441`

```dockerfile
```

-	Layers:
	-	`sha256:b87c115665c3f7e88b3595825828f2bfd7c869b6b38da7ee1325abad95f30db1`  
		Last Modified: Fri, 15 Aug 2025 18:20:47 GMT  
		Size: 18.9 KB (18870 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:55182b60b8fdb5e3d7cde85507b1a8780e863c814ded7a044795cb1e3d1aaa62
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

### `varnish:7.6-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:2e28523af3ac62ce8f5df5f1f528566614755c5d894c54344910267bd3014915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80360313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beadf1b6133d1fb4e2ed6c98af3b2abe24491418b6463974072b0e660e4bd4c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68d422905e258b2c06abba33d7cac42168221aae0303a010a04f88ab2a23e55`  
		Last Modified: Fri, 15 Aug 2025 16:56:55 GMT  
		Size: 76.6 MB (76558565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85a4d5fc6a71c879deaaffde6d40e4a3760be40258c90c7d95a7fe88d79d83d`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3efcf70e77659dfca5f522a6ac025643e281dc719b7a6fbb9426e52547e3aa`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2f2c53f07fd781d6b92cde6bd8a0200ef8e46f8078da33daad6189adf566ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f6e344f9f5a29380d92ff128e32536769ed41f708a1f252ae37d52158098c`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a2d976a799d47c2d5fc2781e7b8b0fc7629e7f5255e105572a894d111c352`  
		Last Modified: Fri, 15 Aug 2025 18:20:48 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:379bab88ceec859e19e44981f502567af57036b8ff5a8c69a4b6a232ce630d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a3bb0cfd3e7e60866c632497e1ed49c3968ca3cf81914657a2587d5311bb90`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be65ae8220b17cebc4940557f2bbca478767709227469272b08f5ced5579884`  
		Last Modified: Fri, 15 Aug 2025 18:21:21 GMT  
		Size: 59.1 MB (59137869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb95b95fe2980a84518f818b4cb4edb91d42de110d0e72f16514ccb0e006797`  
		Last Modified: Fri, 15 Aug 2025 17:37:26 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86919752bd9d80fb2171c0558735ef137e8ddae97d261f939e8b2a627b5177`  
		Last Modified: Fri, 15 Aug 2025 17:37:26 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e48b51726d379095a17ac602baeedb7467118f85e0cc52f14ea3df8fd9527151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcab1367b7d94d5e25fbc2d6964558b907332f898b1b2fc98d669a379e1e827`

```dockerfile
```

-	Layers:
	-	`sha256:455ea1d61388ff00a462eef0e62d92f4b9bd1a3033652833b25971ad2b87b955`  
		Last Modified: Fri, 15 Aug 2025 18:20:51 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:01f30396ee7885727a37b05f4ceeb938e73272c8f89b31c54310fb83686707df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77352942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff942430636abfe637f6deb2253b3ba9195b9bd093f984e40e8f695771520335`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0973e7274fbb6bb2d79f5f57dfa272b575144ab267d6a557fdc4df744c0b74`  
		Last Modified: Fri, 15 Aug 2025 17:02:44 GMT  
		Size: 73.2 MB (73220136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65416659d0fee5f6390111a1ec275b5f477e16c962c32a015f9a1aefb7a4d6`  
		Last Modified: Fri, 15 Aug 2025 17:02:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f872359234a71fdbc0b46bae9130c45f63743ed2f5988bf0d976f1ebb1c81d6d`  
		Last Modified: Fri, 15 Aug 2025 17:02:39 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7022499599f7d49c6495b5860eb8fae5768054eb8c5f2ba91994c43a98eaf286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa2a3c79d99a04a7c2f6b871415d4f46fb3b2ed016ab9845c9ca8cf1ee62ba`

```dockerfile
```

-	Layers:
	-	`sha256:1a816257add10eeb647349f6132d182818df3486dfbdc16ea6d187a87617d3b0`  
		Last Modified: Fri, 15 Aug 2025 18:20:54 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:8c954b7c4405960ec73f5b9499efa166879e3833b0f19d30fffbf5bc8687b718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82580620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f903a36f5ec669127c6300b7d209aaecff97df86bdab35c05a2759e8faa95`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15d6e5299710cb5dac41d28835746591e5c014d20c9f7f59e709acd8b6bfa9`  
		Last Modified: Fri, 15 Aug 2025 16:56:54 GMT  
		Size: 79.0 MB (78963559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6985a2ac50be822aabc113ad078cecb13cfdac13f050dc4d848af2bb863be`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2738232ef9048b3d2198553c94078c35c3411d9238481dc8a1612f81fb6461`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a7d4573bd79febe0431d5079c48652a8ee5ea0b7468744bdfcd7ba621eddb53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911f14009c07b52f51cbb0687d7be87cd14c2ece0eb64130467fde8faa6dc840`

```dockerfile
```

-	Layers:
	-	`sha256:c18a7c2a195c59ca73c6a808b6cdf7eec2d29d151a8a2a7ae533fb8536370a70`  
		Last Modified: Fri, 15 Aug 2025 18:20:58 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b5cc2effed9d3c96575813c9ae309e4960db421a496cf58e385b94ed61b4ac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76484344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08567c3f69380d78bfe7e2ef06e32db6111c54cc25650a124212b2d5449edd2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6adaf6b71bfb3b3d4d0ba7ed33358cd92e00982fe08244fba3852b9dd12ca`  
		Last Modified: Fri, 15 Aug 2025 17:08:01 GMT  
		Size: 72.8 MB (72755174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458b177cd2bd3f4be3d8851688aeb8c640756a34ae684c9b69edf5d151794f09`  
		Last Modified: Fri, 15 Aug 2025 17:07:58 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b90bc979cc22ae747545bdc0a3573ef5709d682e7698b78fd384b5c7d988b3`  
		Last Modified: Fri, 15 Aug 2025 17:07:58 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2dd7232cbb0c05ba7d9bdc08242f54049d0b87b3bce079343fb48221516a9188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a41a0d8ab9703a676ba00d7c43045fde0e751484dd3bce7bdede95d9d8bb20`

```dockerfile
```

-	Layers:
	-	`sha256:1d7949d6c0cde8823ab8ec84f441a8a4584c5a89230d42d8e3d52ca0aa77fcef`  
		Last Modified: Fri, 15 Aug 2025 18:21:01 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:418964a60a086568bf3c9e24c151fc6fdf49daca5770be03811a399f1629591d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71137048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec28ce9e35799416d5561fa764a0166f74b2242c440060cc18dcf2b605909cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f85783785f4a910b12b3142daf7b9792b10396fde68fd61c9942aacd69a210`  
		Last Modified: Fri, 15 Aug 2025 17:05:06 GMT  
		Size: 67.5 MB (67490017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e26276b94a3776f76510bb59649174ea49218dce0cb142ade303c1e895c76`  
		Last Modified: Fri, 15 Aug 2025 17:04:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1afe2786b0558220edbb297ad06dac559501792e8cdc14f08f15a51966f41`  
		Last Modified: Fri, 15 Aug 2025 17:04:46 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4adc40aa798e4122db270aee5f3769196a6c13585fcda05dcc5165073d9f3323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb03c38bf58b26da7e3da97acbb77b9256d2421857e9a3feff783b01427d630d`

```dockerfile
```

-	Layers:
	-	`sha256:e18057a42643b81492b6588dbbf5c71b2a3256d69d3055bc5be864b4d1ab7bb2`  
		Last Modified: Fri, 15 Aug 2025 18:21:05 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.4`

```console
$ docker pull varnish@sha256:55ac9db07a2b148fa275604f15a9b94f26445c54e11e1701f9ffe9729616ee37
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

### `varnish:7.6.4` - linux; amd64

```console
$ docker pull varnish@sha256:a1fb2f20c12438ef482bf8149aece9528fdd8b24b6343ffa182a843889d7c2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109935364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a4d0525acdefa194b1cc9c28c9af7c752cc3cac711727419f40e73fa7fc387`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09267f7e5a383c22b01ad0bf5b02384b7345434b494f8a60bc90cdfb66934070`  
		Last Modified: Fri, 15 Aug 2025 16:57:49 GMT  
		Size: 81.7 MB (81703064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6f128744545326a15166b51afb3e08827e5cf2afdb7f60b6ce1208e3e95d14`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6829a15a5bc04c257c64e3468ee5f3e0b43ff44a6eab0e3d7382967f444045`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:c222ef3b761cd4101767ce05ce4b3e7c56239128bc44e89e672e855647aecfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0556654bf18f33829c58cf35fca961103727c4188d34ec864fd5202871997ec6`

```dockerfile
```

-	Layers:
	-	`sha256:49690a315c3e50f7eb6d14c4bef2ef21a322a1b4e5310dba968ac567847b216c`  
		Last Modified: Fri, 15 Aug 2025 18:20:31 GMT  
		Size: 18.9 KB (18871 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; arm variant v7

```console
$ docker pull varnish@sha256:2dde0e165d54e25b0e0a42fcd98da86647a66f3cb6b28156330959b50e764370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82185203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc70aba460a17488c1dcffa90c4ac199283b309d2c4e24f5ca0de078f1dc599b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c482092d910c7110f0605ae4db82097e5f488b42c827f8abe3baea139c9535a`  
		Last Modified: Fri, 15 Aug 2025 17:01:45 GMT  
		Size: 58.2 MB (58244224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a4c5dacace037dd116a534d3e2e6cf0061119c6b1c5418734ba783d7515ad`  
		Last Modified: Fri, 15 Aug 2025 17:01:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fd9c49bf7a0d3736d7214af56dfed1230f54a846dc3380c17540eee10dd1f2`  
		Last Modified: Fri, 15 Aug 2025 17:01:35 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:2b37a8c98eee509364d75ab8f563bde11976bfd70be7c499813659cbc2745ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617b048a15b0acca175b3a678db24692ca8cfacf6796525c717a1c4654c3f5`

```dockerfile
```

-	Layers:
	-	`sha256:6eba3dcedecd35442cb775edd859623bab177e01b7febc0e98b174e0cd568939`  
		Last Modified: Fri, 15 Aug 2025 18:20:35 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8b7c11552292d531475f0d54463beae68da5bdf7d859eb1a83a47afb479f270a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104449591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fa7fde6ec1a84fba9665510b54fdb2994fb2735d988f99e5778aa3b42bf80b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd0936b3e7a1906e0dcd9f67846122080e0fa52bd067c4fb7fc279ae847d0c`  
		Last Modified: Fri, 15 Aug 2025 17:01:23 GMT  
		Size: 76.4 MB (76365546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21739974fa1f38fd215745094ac2db46becce16d34d034a3a2c3c8e62a0987ea`  
		Last Modified: Fri, 15 Aug 2025 17:01:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c890712c0af0dc42f3c1a1a7db2493a3c986de76bea5c7ee6ead7a2911a6f43b`  
		Last Modified: Fri, 15 Aug 2025 17:01:16 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:e934bfe8943e75dbd1d6bcd8e27048c270da9c865168d9a88dbed68bf1c77328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b43d13e42577bd39579d32bbf27a9a995b8b310bb766e1358677b0c0d6688cd`

```dockerfile
```

-	Layers:
	-	`sha256:6a38d12aa59e268d53752119c2808a8922cf235d7335eaf0b0f450cd0afdfb93`  
		Last Modified: Fri, 15 Aug 2025 18:20:38 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; 386

```console
$ docker pull varnish@sha256:10a5db2b243687d760fa20c79999a7c632b4691793acc4dd1a5d95356d02db16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107339580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd50e7d7df3a4b515a1c8ae46a155d2c5bf426c62db280ca2fa8365071bca83`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c62e81843249b5cb46ac342e6453be1c2b9d3b959437306a9a077d403976b3`  
		Last Modified: Fri, 15 Aug 2025 16:57:46 GMT  
		Size: 78.1 MB (78124931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc091cc50d8ccb50f08b1eddff8c15d443ddee40df8eabcd21c594d5826f44f5`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1922589f9b12760e939f8eb0c74c48a75dcaf00c702c049b7b360aa83c15288a`  
		Last Modified: Fri, 15 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:7ee892531be69de90be55946b0a76a0c6ddc8be3a38696bf99e733b2362a0f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec6abd510c3912a99835ec879a9914911d4495ac9f7d6063b3f7a036839c6a9`

```dockerfile
```

-	Layers:
	-	`sha256:9b42f2b3d67bc1dbd8f2ba77391f5a5562ae5eaf1da2f64250db6463a0ee8589`  
		Last Modified: Fri, 15 Aug 2025 18:20:41 GMT  
		Size: 18.8 KB (18844 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; ppc64le

```console
$ docker pull varnish@sha256:d771d0a11e5cb044fb29e243105d0fbaab24c34f772c4e6161e5e6cc6e2aae36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111970696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7fbf7aea862f1ce5f5b6743855ca732d0f26f5bf013b2bab03fd7e6a722e56`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f128671fcf877380ff6584510acfe5b88b91f2658c3348c827730b222267a31`  
		Last Modified: Fri, 15 Aug 2025 17:21:02 GMT  
		Size: 79.9 MB (79895231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981a0080d7c508255eac372f3977fbeb18600432db4ca13c65d3a567527af707`  
		Last Modified: Fri, 15 Aug 2025 17:20:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8407d8692a211522d3327eafc25ce587b9c952337fd433bb34be66bbd2517b`  
		Last Modified: Fri, 15 Aug 2025 17:20:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:479a8356add5b245a038ab07bb03f40962d410e4cff3fe671f0c3c35c7c45c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d3f1bc54dacefb5e68e75b5ccd1a117df8d285362cc6e80737b2fa1efe994d`

```dockerfile
```

-	Layers:
	-	`sha256:08ec36e5441b3a6da7a97f757f3e01f7b9a3d321e129455be42b51382a74a2fc`  
		Last Modified: Fri, 15 Aug 2025 18:20:44 GMT  
		Size: 18.9 KB (18909 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; s390x

```console
$ docker pull varnish@sha256:b42f11c5699d210935309a878e399a8123e82e28ff9753c2ade5c960aa5d7080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87740299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be0ad2520373e21bff38de538ae40b78fd68435c1fdc6f4a3a7acbbb6b1932a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eb726fb2e8bff58331cf376c5c7a5e8696a9d03c548971766e4d1cbeb15097`  
		Last Modified: Fri, 15 Aug 2025 17:03:06 GMT  
		Size: 60.9 MB (60850415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b6eba540f8219227bdcc54c0371204b3f3e02094a4c5a5ab53d8970c51f0f3`  
		Last Modified: Fri, 15 Aug 2025 17:02:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac740b1ffc0d320f134e48c4c99a02b78cfb4d5948a7df22a6866d238d1acace`  
		Last Modified: Fri, 15 Aug 2025 17:02:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:50a68b601ee2b9d22d4ea3e1451db8ff2fdbf0992d3c6ed06becf9ecd3d6d75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751bfecbd724e325e691d6c1a0716f9f5d6fa5a454980a62a1e9afa46aff0441`

```dockerfile
```

-	Layers:
	-	`sha256:b87c115665c3f7e88b3595825828f2bfd7c869b6b38da7ee1325abad95f30db1`  
		Last Modified: Fri, 15 Aug 2025 18:20:47 GMT  
		Size: 18.9 KB (18870 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.4-alpine`

```console
$ docker pull varnish@sha256:55182b60b8fdb5e3d7cde85507b1a8780e863c814ded7a044795cb1e3d1aaa62
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

### `varnish:7.6.4-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:2e28523af3ac62ce8f5df5f1f528566614755c5d894c54344910267bd3014915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80360313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beadf1b6133d1fb4e2ed6c98af3b2abe24491418b6463974072b0e660e4bd4c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68d422905e258b2c06abba33d7cac42168221aae0303a010a04f88ab2a23e55`  
		Last Modified: Fri, 15 Aug 2025 16:56:55 GMT  
		Size: 76.6 MB (76558565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85a4d5fc6a71c879deaaffde6d40e4a3760be40258c90c7d95a7fe88d79d83d`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3efcf70e77659dfca5f522a6ac025643e281dc719b7a6fbb9426e52547e3aa`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2f2c53f07fd781d6b92cde6bd8a0200ef8e46f8078da33daad6189adf566ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f6e344f9f5a29380d92ff128e32536769ed41f708a1f252ae37d52158098c`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a2d976a799d47c2d5fc2781e7b8b0fc7629e7f5255e105572a894d111c352`  
		Last Modified: Fri, 15 Aug 2025 18:20:48 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:379bab88ceec859e19e44981f502567af57036b8ff5a8c69a4b6a232ce630d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a3bb0cfd3e7e60866c632497e1ed49c3968ca3cf81914657a2587d5311bb90`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be65ae8220b17cebc4940557f2bbca478767709227469272b08f5ced5579884`  
		Last Modified: Fri, 15 Aug 2025 18:21:21 GMT  
		Size: 59.1 MB (59137869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb95b95fe2980a84518f818b4cb4edb91d42de110d0e72f16514ccb0e006797`  
		Last Modified: Fri, 15 Aug 2025 17:37:26 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86919752bd9d80fb2171c0558735ef137e8ddae97d261f939e8b2a627b5177`  
		Last Modified: Fri, 15 Aug 2025 17:37:26 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e48b51726d379095a17ac602baeedb7467118f85e0cc52f14ea3df8fd9527151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcab1367b7d94d5e25fbc2d6964558b907332f898b1b2fc98d669a379e1e827`

```dockerfile
```

-	Layers:
	-	`sha256:455ea1d61388ff00a462eef0e62d92f4b9bd1a3033652833b25971ad2b87b955`  
		Last Modified: Fri, 15 Aug 2025 18:20:51 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:01f30396ee7885727a37b05f4ceeb938e73272c8f89b31c54310fb83686707df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77352942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff942430636abfe637f6deb2253b3ba9195b9bd093f984e40e8f695771520335`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0973e7274fbb6bb2d79f5f57dfa272b575144ab267d6a557fdc4df744c0b74`  
		Last Modified: Fri, 15 Aug 2025 17:02:44 GMT  
		Size: 73.2 MB (73220136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65416659d0fee5f6390111a1ec275b5f477e16c962c32a015f9a1aefb7a4d6`  
		Last Modified: Fri, 15 Aug 2025 17:02:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f872359234a71fdbc0b46bae9130c45f63743ed2f5988bf0d976f1ebb1c81d6d`  
		Last Modified: Fri, 15 Aug 2025 17:02:39 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7022499599f7d49c6495b5860eb8fae5768054eb8c5f2ba91994c43a98eaf286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa2a3c79d99a04a7c2f6b871415d4f46fb3b2ed016ab9845c9ca8cf1ee62ba`

```dockerfile
```

-	Layers:
	-	`sha256:1a816257add10eeb647349f6132d182818df3486dfbdc16ea6d187a87617d3b0`  
		Last Modified: Fri, 15 Aug 2025 18:20:54 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4-alpine` - linux; 386

```console
$ docker pull varnish@sha256:8c954b7c4405960ec73f5b9499efa166879e3833b0f19d30fffbf5bc8687b718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82580620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f903a36f5ec669127c6300b7d209aaecff97df86bdab35c05a2759e8faa95`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15d6e5299710cb5dac41d28835746591e5c014d20c9f7f59e709acd8b6bfa9`  
		Last Modified: Fri, 15 Aug 2025 16:56:54 GMT  
		Size: 79.0 MB (78963559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6985a2ac50be822aabc113ad078cecb13cfdac13f050dc4d848af2bb863be`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2738232ef9048b3d2198553c94078c35c3411d9238481dc8a1612f81fb6461`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a7d4573bd79febe0431d5079c48652a8ee5ea0b7468744bdfcd7ba621eddb53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911f14009c07b52f51cbb0687d7be87cd14c2ece0eb64130467fde8faa6dc840`

```dockerfile
```

-	Layers:
	-	`sha256:c18a7c2a195c59ca73c6a808b6cdf7eec2d29d151a8a2a7ae533fb8536370a70`  
		Last Modified: Fri, 15 Aug 2025 18:20:58 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b5cc2effed9d3c96575813c9ae309e4960db421a496cf58e385b94ed61b4ac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76484344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08567c3f69380d78bfe7e2ef06e32db6111c54cc25650a124212b2d5449edd2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6adaf6b71bfb3b3d4d0ba7ed33358cd92e00982fe08244fba3852b9dd12ca`  
		Last Modified: Fri, 15 Aug 2025 17:08:01 GMT  
		Size: 72.8 MB (72755174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458b177cd2bd3f4be3d8851688aeb8c640756a34ae684c9b69edf5d151794f09`  
		Last Modified: Fri, 15 Aug 2025 17:07:58 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b90bc979cc22ae747545bdc0a3573ef5709d682e7698b78fd384b5c7d988b3`  
		Last Modified: Fri, 15 Aug 2025 17:07:58 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2dd7232cbb0c05ba7d9bdc08242f54049d0b87b3bce079343fb48221516a9188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a41a0d8ab9703a676ba00d7c43045fde0e751484dd3bce7bdede95d9d8bb20`

```dockerfile
```

-	Layers:
	-	`sha256:1d7949d6c0cde8823ab8ec84f441a8a4584c5a89230d42d8e3d52ca0aa77fcef`  
		Last Modified: Fri, 15 Aug 2025 18:21:01 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:418964a60a086568bf3c9e24c151fc6fdf49daca5770be03811a399f1629591d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71137048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec28ce9e35799416d5561fa764a0166f74b2242c440060cc18dcf2b605909cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f85783785f4a910b12b3142daf7b9792b10396fde68fd61c9942aacd69a210`  
		Last Modified: Fri, 15 Aug 2025 17:05:06 GMT  
		Size: 67.5 MB (67490017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e26276b94a3776f76510bb59649174ea49218dce0cb142ade303c1e895c76`  
		Last Modified: Fri, 15 Aug 2025 17:04:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1afe2786b0558220edbb297ad06dac559501792e8cdc14f08f15a51966f41`  
		Last Modified: Fri, 15 Aug 2025 17:04:46 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4adc40aa798e4122db270aee5f3769196a6c13585fcda05dcc5165073d9f3323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb03c38bf58b26da7e3da97acbb77b9256d2421857e9a3feff783b01427d630d`

```dockerfile
```

-	Layers:
	-	`sha256:e18057a42643b81492b6588dbbf5c71b2a3256d69d3055bc5be864b4d1ab7bb2`  
		Last Modified: Fri, 15 Aug 2025 18:21:05 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:83ca6fecb7781cf39d4489bad0d357d20a8edb943f5563b90ff46d94360f4ff2
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

### `varnish:7.7` - linux; amd64

```console
$ docker pull varnish@sha256:fedfa20758d2651daf48ce3ae0c252539ec834fb1d8371335b8f13538c3d00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110106279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f281d5b0ed5e1cde6a33baf7c1a3f71055bd16d781940ec42a1a6be11bca5144`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767674a186da8285836153cb726409d4112a4a80fc976127bdf22c5df07a342`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 81.9 MB (81873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a35607832b0b15801f55356a07a24586b93213ef9a8d0c65fddc881463143`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddb218959aa0785586687d3d0aec6ce87943c57d054025007ae3f5f5780c5e`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:0e470651a8e0394799e7bbdf63d667730f87b8031f5db0a6d6dcfcc9aab04caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9b00d45d0fad1c56cab3e0d94f609b0838c8cd95edbd9e43910024dab3c76`

```dockerfile
```

-	Layers:
	-	`sha256:093b8a36638c67c6ebd86a569d5a9e880125463b6121e13cb842711c247e53df`  
		Last Modified: Fri, 15 Aug 2025 18:20:01 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6ef60b34629736d2141c8fb33ab6c2ea3a6a24b49a8cd2734b5c616daf0b8ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82361579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65f47712081b446c96886e6775c5643a2e8b77b1f93bafdc4d9060c488ae3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865acd02bf9c4f607ff081eacbcc80167f492e47029b6f33665a0092132885a`  
		Last Modified: Fri, 15 Aug 2025 16:57:09 GMT  
		Size: 58.4 MB (58420605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a9cb9947510c533811bb4f8ea48b8875ecdfcd746a0059cfb266744b2edb6`  
		Last Modified: Fri, 15 Aug 2025 16:57:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829b90f4f1f7509e840ecadd5046ff17ad077e9fffa3d6045fdd90d2b67b3ec`  
		Last Modified: Fri, 15 Aug 2025 16:57:05 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:5a95c4e9bdbda53ac19a4f7eb2fc7871c27bc54ec62f465520f9fed03f72c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ad9b4ae87f0700a77508ce6db54194c580d23dd71847fd987a3c2785c4571`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcf08c3380eaf1388cd59017438b8bfecd643cca66768e2856226c4b8100ce`  
		Last Modified: Fri, 15 Aug 2025 18:20:04 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c022a0ff5f7d30d8d65cdd3aad6a97f02e4d2bf8b551977c74d3e6784a78db30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9ba230852531c6b2deb4e5aebc846e12855d713a6f1daadb2367d71cd98992`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121caf58da77aa0443a2496d57c85ea79d8e1df2405a26b8d5e3673b479bf20`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 76.5 MB (76538135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec5280a3b9e492d66687c59a64df4f0f155ba5207db69037007ae5fde08120`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37110db52b9ecad7c7a879bb96852fe0ef35b0ece8dd3887a49bec4d0dfc3f3b`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:751a4801d5a9c5f699faad34be2f5905b06088ed10bf52f8b0b80ca728645a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664d38510adf7bbc0020d7dca45643c6126b6c65e459171cc4d00fe610eb1d2`

```dockerfile
```

-	Layers:
	-	`sha256:cf2d904d3d707278b34f5a4903707327e72e00baf0ae5df1a13efedb5d611426`  
		Last Modified: Fri, 15 Aug 2025 18:20:08 GMT  
		Size: 19.6 KB (19572 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

```console
$ docker pull varnish@sha256:643e67a2f50b57bca50e83839f7f8b91b3c47588dd396769ede34e6db05e44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107508252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db414121d0e199a39b26554aef75af674c08942370d3c88386de0e1d008c1572`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a29dc117e0a7cf8a15e635b05ccf4d12c7a1ee6067cf3f182e71f264226655`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 78.3 MB (78293602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d90c530a68e0fbb406e32d98113522350b1170c276aaa0c300ec0cd5d34471`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020470a039d54dd250c2e33a0b7ad201a5a7dde161b96dd8aa20f54f65eb06d4`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:e403282207a41140505699aa134579847e5933b7c004aed9a357a12333a68bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c959bbaebf235be5668c87882884c538a7ba91403725fa4595ae53166076fbd`

```dockerfile
```

-	Layers:
	-	`sha256:9670f5aac7a9527cbdff76983554c8c1405a95db2b3b9ce78a62e32be01562b5`  
		Last Modified: Fri, 15 Aug 2025 18:20:11 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; ppc64le

```console
$ docker pull varnish@sha256:5d63d6d9b3a816d335ab85a7fd3c24f078e8661c94d90f82cebdb65328894de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112125451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855097713d44be414c5475db87bcaa3807ac765b8529db689eff325ef52a983`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063bcd1ca526e732f14ddda8346106790e36b532d8f7ebbd7939f1f3390c975b`  
		Last Modified: Fri, 15 Aug 2025 17:00:10 GMT  
		Size: 80.0 MB (80049983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71734c96c8bc5b7e443557665eeda472a075a5cd5a0ac09e3b768ccbda14da8`  
		Last Modified: Fri, 15 Aug 2025 17:00:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b495f9c9889d394cacb9be69d494dc4f799f756dd6b652c7771f56bb6a8f82`  
		Last Modified: Fri, 15 Aug 2025 17:00:05 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:85986ce2cb4509cb6fa45a8f3c09981811c4036abad32fb472dd68250e65163a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dffec5d24b702fc55c635da910ac3d0da72d6da380f0d1e227dc9278646f6f`

```dockerfile
```

-	Layers:
	-	`sha256:a1646d6d4130c7e1c7b72eefc76d27ca9be0ce2306db99bbe68a55856ac896c3`  
		Last Modified: Fri, 15 Aug 2025 18:20:14 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; s390x

```console
$ docker pull varnish@sha256:9141e45c7cd14117b58069fd59d4cc53c8badaeade8f9a536092c8143aa8e571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87911883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45dd74ae8f7452e7c68d37c305c66ffed0cac781869788d41e4882e352c37cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead03c3e8d7cd776db98c9f94e1610ca909dddfc22e62d793c6301988e7b4a97`  
		Last Modified: Fri, 15 Aug 2025 16:58:16 GMT  
		Size: 61.0 MB (61021999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f194092d9bc42b54e915dbd444d3b36e8d1e5343277b869e660e9ca0886c2b`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beefcc26fe8cb04b79d3ce2dbfeb6e61ce0c3553afc049dcf524ae6c44a25ab`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:4ec9d06a7ed84cb2369aa6497a334a6c5f94ed608f6bf9fd1c15e714d634b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f886ac06337c55578efdad672bd8221a76bfc5292462fb8f685c13c3a755c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f619217400a1c21827da3eb8bcf12dd75b9983fdfc57d3fa43c9fa87674f776`  
		Last Modified: Fri, 15 Aug 2025 18:20:17 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:11f468c0fac3c1c019ed680d37f905a4e97cf4d87d562202ed1ed6dc3054d7c6
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

### `varnish:7.7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:7035c20e4805ab5f70599ef1e4057a1aa57ad7ae2d50f8409a93867f1cae4e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80505421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801bc1bb3b98d83d0802e4e829cc1218ea8134d53b4f06104d9f13978c59f0b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55297ffdb439992b8f725e1abee5cfb1f41f3c26beabd7e2bbb004029148296`  
		Last Modified: Fri, 15 Aug 2025 16:56:50 GMT  
		Size: 76.7 MB (76703672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bd86dfee1e73c6276ee94e788dc89ba827a83d22f4454a2011064fc9f82f4`  
		Last Modified: Fri, 15 Aug 2025 16:56:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539ddb67860c1bfec8f0ac73d49a345cdc44ba46ab1b6da9ef818f68cb290cc`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fff050818c236d2652dff618185a1b092aa7b86c042cf9dc46eb0c5ecc422843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb200068daf0e7aa4cc2e7d0f920c1c9b766b6f86e7ef8224f9c40022498079a`

```dockerfile
```

-	Layers:
	-	`sha256:b233189ccdc4fd3796925be1bb23d5c8269cefe12c4b7b0d123c7f36ffdf4156`  
		Last Modified: Fri, 15 Aug 2025 18:20:16 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9e81fcdb8ea18f49dac62d0e6f2395e6c5d1ebe5b537c2343ebbcdb3dd487397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62515065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9411aaf5f3dbef0e91342c29cf7d595ce30ee60f41d66e3fff2a369f4b1d8dfe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c6c5dcb5b4ac9ad073457a12700618c82623de85fb82f2d5fb326bca6a600`  
		Last Modified: Fri, 15 Aug 2025 16:59:02 GMT  
		Size: 59.3 MB (59293972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d82b3db827a281bb380ace01fc619eaa48d752c82e2fd376a28c752f1465ff5`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97cd2adc93836662f8319b7754daac32766095945bbbd68c407d62f8b7e1d98`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18353cb316e339f32e46a86e9a14cc92c68611618f1d0e7e409c14d87efa920b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fe86f4fcf0d2a0df26272c5ad8251508207e05b0fa78c65a4c02e77d0a1e9b`

```dockerfile
```

-	Layers:
	-	`sha256:eca07e957d3e688c6caee11f6b3e4e3efd6d17f0fbb83518fd0f96c10962a9e5`  
		Last Modified: Fri, 15 Aug 2025 18:20:19 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d6df66a151a86aa3c614afa6279d5bea14710a86ce3dfab839160b94d1e80ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77498564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053598a7edda72857a2903a0b0371938657afa3a81079b4cfae7a9555359b01`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34fadec23958052f927e36d3e2fa9dd9b9ce78567638099bc0d9334feb4d93`  
		Last Modified: Fri, 15 Aug 2025 16:58:43 GMT  
		Size: 73.4 MB (73365758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e96be58cc45f2ba927d34bdf0172d2b8d7377124a996d42e808fdf4cfa3b72`  
		Last Modified: Fri, 15 Aug 2025 16:58:40 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98997d85e5d6da9c6d5dbf443b23fdcf0669368bd779025a5a1aa111a07e05f`  
		Last Modified: Fri, 15 Aug 2025 16:58:41 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2561dd56ac33c571b7b332395ece35ab92caa03f3829fa1196b1c368651cdbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b4eadb528c844dd226ae97105b841aa3bdec59d3be2ebd796fec7b00c04d54`

```dockerfile
```

-	Layers:
	-	`sha256:40af3552a2a3f4340d8e17e4d4daabf005c1c861aa2e8c1c1bb700cbcaeed15d`  
		Last Modified: Fri, 15 Aug 2025 18:20:22 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9a1c3998552633081142f8c46765d5f54144dbfa64f3433e87faddf2c883d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3709c2147eee9862efa2559144884bb8f59697f031c38c5f4e2fd36d829454e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5273443b55588922d029ea0a105bcef20161f7347f7723a8a2bf00ba5409c29`  
		Last Modified: Fri, 15 Aug 2025 18:20:52 GMT  
		Size: 79.1 MB (79115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5306d254fb0902aa4460d62f07845d4308e97c4f36214af53ad59455348b0`  
		Last Modified: Fri, 15 Aug 2025 17:27:23 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd7e5a4c259b0e2da55fdcc2a951ff2d4e57059a085970ba0a2a457820011b`  
		Last Modified: Fri, 15 Aug 2025 17:27:22 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:805ac3dbf45f6e2a1dbf9817a7b6a69e3226fdb19a16bb57330437319a30c730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9395e2b144bc8f7bc98fe149d18657a2e7b81ca6069c270aa4bd292983f413c`

```dockerfile
```

-	Layers:
	-	`sha256:817b6ca8afcbee4bba4d42bd3193dce131fa0fee46f80e1ba8c59a36877f5c1c`  
		Last Modified: Fri, 15 Aug 2025 18:20:26 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:4013273c17e4d73d0fff79e87e82d992487316c0462b023c2127b71d02b30ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76633537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d930a8ffe8c5620edda4a5ae4083beca22509b76dcca3f020352b803f9fa06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace93df466c17cd7ca7913c595aa0c794ea5fbd619f8289dcc0542b678139a1`  
		Last Modified: Fri, 15 Aug 2025 17:15:37 GMT  
		Size: 72.9 MB (72904365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98130a78b774a02fd26aae942aa7184d419e13cb2f08db2862a314215672524b`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9bc2376dfa75b485a5fcf0d9ffc4339b721217e78d0301c550afd8852dd93c`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b782e164fdc8b81adc6e74b39ae3b241c8a92987d16b383bc97a03b90d718e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230eaceef94b90468bf978df0fa292d7206e25542088ae0d930c0646ae9d272`

```dockerfile
```

-	Layers:
	-	`sha256:3cf726d2f7ef3fe6dc191ab3cfc4480ee577512d43c5c480b633013e45b4c749`  
		Last Modified: Fri, 15 Aug 2025 18:20:29 GMT  
		Size: 19.5 KB (19518 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:be77e8e657b601fa610f69d3c57c0d2477b9b7114b173dde5602654fd5d0416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89093a7ecc822c5b6def0853f54aee46c86cd4eb988f9c443e962fb9f0254f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b4cd4d200db742fc36965160bffa32a4266c50fe01a3a3098c5dd0c6f6ca6`  
		Last Modified: Fri, 15 Aug 2025 17:00:11 GMT  
		Size: 67.6 MB (67637480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd6b2622d0e954a05bede36e6c5572d4003aaca0a717adbcafc33fe4b9de7f`  
		Last Modified: Fri, 15 Aug 2025 17:00:06 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671b8de9982d6140e072fc678c363fb0760ca978dcfdcd4721579178cf7402e`  
		Last Modified: Fri, 15 Aug 2025 17:00:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4d661ac5f10739ea3990846451b229f77886a428fb934502f7809c628bbe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e5a16b6b5c9085598ef0af0b1290c2dee11db9794440119a10ed5d01fcec2`

```dockerfile
```

-	Layers:
	-	`sha256:c3364ad35a3f174f668207d29078228dc7d165a94b113fdb93703a0b7fa2b1a9`  
		Last Modified: Fri, 15 Aug 2025 18:20:32 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.2`

```console
$ docker pull varnish@sha256:83ca6fecb7781cf39d4489bad0d357d20a8edb943f5563b90ff46d94360f4ff2
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

### `varnish:7.7.2` - linux; amd64

```console
$ docker pull varnish@sha256:fedfa20758d2651daf48ce3ae0c252539ec834fb1d8371335b8f13538c3d00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110106279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f281d5b0ed5e1cde6a33baf7c1a3f71055bd16d781940ec42a1a6be11bca5144`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767674a186da8285836153cb726409d4112a4a80fc976127bdf22c5df07a342`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 81.9 MB (81873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a35607832b0b15801f55356a07a24586b93213ef9a8d0c65fddc881463143`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddb218959aa0785586687d3d0aec6ce87943c57d054025007ae3f5f5780c5e`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2` - unknown; unknown

```console
$ docker pull varnish@sha256:0e470651a8e0394799e7bbdf63d667730f87b8031f5db0a6d6dcfcc9aab04caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9b00d45d0fad1c56cab3e0d94f609b0838c8cd95edbd9e43910024dab3c76`

```dockerfile
```

-	Layers:
	-	`sha256:093b8a36638c67c6ebd86a569d5a9e880125463b6121e13cb842711c247e53df`  
		Last Modified: Fri, 15 Aug 2025 18:20:01 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6ef60b34629736d2141c8fb33ab6c2ea3a6a24b49a8cd2734b5c616daf0b8ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82361579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65f47712081b446c96886e6775c5643a2e8b77b1f93bafdc4d9060c488ae3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865acd02bf9c4f607ff081eacbcc80167f492e47029b6f33665a0092132885a`  
		Last Modified: Fri, 15 Aug 2025 16:57:09 GMT  
		Size: 58.4 MB (58420605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a9cb9947510c533811bb4f8ea48b8875ecdfcd746a0059cfb266744b2edb6`  
		Last Modified: Fri, 15 Aug 2025 16:57:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829b90f4f1f7509e840ecadd5046ff17ad077e9fffa3d6045fdd90d2b67b3ec`  
		Last Modified: Fri, 15 Aug 2025 16:57:05 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2` - unknown; unknown

```console
$ docker pull varnish@sha256:5a95c4e9bdbda53ac19a4f7eb2fc7871c27bc54ec62f465520f9fed03f72c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ad9b4ae87f0700a77508ce6db54194c580d23dd71847fd987a3c2785c4571`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcf08c3380eaf1388cd59017438b8bfecd643cca66768e2856226c4b8100ce`  
		Last Modified: Fri, 15 Aug 2025 18:20:04 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c022a0ff5f7d30d8d65cdd3aad6a97f02e4d2bf8b551977c74d3e6784a78db30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9ba230852531c6b2deb4e5aebc846e12855d713a6f1daadb2367d71cd98992`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121caf58da77aa0443a2496d57c85ea79d8e1df2405a26b8d5e3673b479bf20`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 76.5 MB (76538135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec5280a3b9e492d66687c59a64df4f0f155ba5207db69037007ae5fde08120`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37110db52b9ecad7c7a879bb96852fe0ef35b0ece8dd3887a49bec4d0dfc3f3b`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2` - unknown; unknown

```console
$ docker pull varnish@sha256:751a4801d5a9c5f699faad34be2f5905b06088ed10bf52f8b0b80ca728645a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664d38510adf7bbc0020d7dca45643c6126b6c65e459171cc4d00fe610eb1d2`

```dockerfile
```

-	Layers:
	-	`sha256:cf2d904d3d707278b34f5a4903707327e72e00baf0ae5df1a13efedb5d611426`  
		Last Modified: Fri, 15 Aug 2025 18:20:08 GMT  
		Size: 19.6 KB (19572 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2` - linux; 386

```console
$ docker pull varnish@sha256:643e67a2f50b57bca50e83839f7f8b91b3c47588dd396769ede34e6db05e44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107508252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db414121d0e199a39b26554aef75af674c08942370d3c88386de0e1d008c1572`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a29dc117e0a7cf8a15e635b05ccf4d12c7a1ee6067cf3f182e71f264226655`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 78.3 MB (78293602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d90c530a68e0fbb406e32d98113522350b1170c276aaa0c300ec0cd5d34471`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020470a039d54dd250c2e33a0b7ad201a5a7dde161b96dd8aa20f54f65eb06d4`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2` - unknown; unknown

```console
$ docker pull varnish@sha256:e403282207a41140505699aa134579847e5933b7c004aed9a357a12333a68bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c959bbaebf235be5668c87882884c538a7ba91403725fa4595ae53166076fbd`

```dockerfile
```

-	Layers:
	-	`sha256:9670f5aac7a9527cbdff76983554c8c1405a95db2b3b9ce78a62e32be01562b5`  
		Last Modified: Fri, 15 Aug 2025 18:20:11 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2` - linux; ppc64le

```console
$ docker pull varnish@sha256:5d63d6d9b3a816d335ab85a7fd3c24f078e8661c94d90f82cebdb65328894de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112125451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855097713d44be414c5475db87bcaa3807ac765b8529db689eff325ef52a983`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063bcd1ca526e732f14ddda8346106790e36b532d8f7ebbd7939f1f3390c975b`  
		Last Modified: Fri, 15 Aug 2025 17:00:10 GMT  
		Size: 80.0 MB (80049983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71734c96c8bc5b7e443557665eeda472a075a5cd5a0ac09e3b768ccbda14da8`  
		Last Modified: Fri, 15 Aug 2025 17:00:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b495f9c9889d394cacb9be69d494dc4f799f756dd6b652c7771f56bb6a8f82`  
		Last Modified: Fri, 15 Aug 2025 17:00:05 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2` - unknown; unknown

```console
$ docker pull varnish@sha256:85986ce2cb4509cb6fa45a8f3c09981811c4036abad32fb472dd68250e65163a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dffec5d24b702fc55c635da910ac3d0da72d6da380f0d1e227dc9278646f6f`

```dockerfile
```

-	Layers:
	-	`sha256:a1646d6d4130c7e1c7b72eefc76d27ca9be0ce2306db99bbe68a55856ac896c3`  
		Last Modified: Fri, 15 Aug 2025 18:20:14 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2` - linux; s390x

```console
$ docker pull varnish@sha256:9141e45c7cd14117b58069fd59d4cc53c8badaeade8f9a536092c8143aa8e571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87911883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45dd74ae8f7452e7c68d37c305c66ffed0cac781869788d41e4882e352c37cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead03c3e8d7cd776db98c9f94e1610ca909dddfc22e62d793c6301988e7b4a97`  
		Last Modified: Fri, 15 Aug 2025 16:58:16 GMT  
		Size: 61.0 MB (61021999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f194092d9bc42b54e915dbd444d3b36e8d1e5343277b869e660e9ca0886c2b`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beefcc26fe8cb04b79d3ce2dbfeb6e61ce0c3553afc049dcf524ae6c44a25ab`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2` - unknown; unknown

```console
$ docker pull varnish@sha256:4ec9d06a7ed84cb2369aa6497a334a6c5f94ed608f6bf9fd1c15e714d634b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f886ac06337c55578efdad672bd8221a76bfc5292462fb8f685c13c3a755c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f619217400a1c21827da3eb8bcf12dd75b9983fdfc57d3fa43c9fa87674f776`  
		Last Modified: Fri, 15 Aug 2025 18:20:17 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.2-alpine`

```console
$ docker pull varnish@sha256:11f468c0fac3c1c019ed680d37f905a4e97cf4d87d562202ed1ed6dc3054d7c6
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

### `varnish:7.7.2-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:7035c20e4805ab5f70599ef1e4057a1aa57ad7ae2d50f8409a93867f1cae4e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80505421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801bc1bb3b98d83d0802e4e829cc1218ea8134d53b4f06104d9f13978c59f0b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55297ffdb439992b8f725e1abee5cfb1f41f3c26beabd7e2bbb004029148296`  
		Last Modified: Fri, 15 Aug 2025 16:56:50 GMT  
		Size: 76.7 MB (76703672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bd86dfee1e73c6276ee94e788dc89ba827a83d22f4454a2011064fc9f82f4`  
		Last Modified: Fri, 15 Aug 2025 16:56:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539ddb67860c1bfec8f0ac73d49a345cdc44ba46ab1b6da9ef818f68cb290cc`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fff050818c236d2652dff618185a1b092aa7b86c042cf9dc46eb0c5ecc422843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb200068daf0e7aa4cc2e7d0f920c1c9b766b6f86e7ef8224f9c40022498079a`

```dockerfile
```

-	Layers:
	-	`sha256:b233189ccdc4fd3796925be1bb23d5c8269cefe12c4b7b0d123c7f36ffdf4156`  
		Last Modified: Fri, 15 Aug 2025 18:20:16 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9e81fcdb8ea18f49dac62d0e6f2395e6c5d1ebe5b537c2343ebbcdb3dd487397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62515065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9411aaf5f3dbef0e91342c29cf7d595ce30ee60f41d66e3fff2a369f4b1d8dfe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c6c5dcb5b4ac9ad073457a12700618c82623de85fb82f2d5fb326bca6a600`  
		Last Modified: Fri, 15 Aug 2025 16:59:02 GMT  
		Size: 59.3 MB (59293972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d82b3db827a281bb380ace01fc619eaa48d752c82e2fd376a28c752f1465ff5`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97cd2adc93836662f8319b7754daac32766095945bbbd68c407d62f8b7e1d98`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18353cb316e339f32e46a86e9a14cc92c68611618f1d0e7e409c14d87efa920b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fe86f4fcf0d2a0df26272c5ad8251508207e05b0fa78c65a4c02e77d0a1e9b`

```dockerfile
```

-	Layers:
	-	`sha256:eca07e957d3e688c6caee11f6b3e4e3efd6d17f0fbb83518fd0f96c10962a9e5`  
		Last Modified: Fri, 15 Aug 2025 18:20:19 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d6df66a151a86aa3c614afa6279d5bea14710a86ce3dfab839160b94d1e80ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77498564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053598a7edda72857a2903a0b0371938657afa3a81079b4cfae7a9555359b01`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34fadec23958052f927e36d3e2fa9dd9b9ce78567638099bc0d9334feb4d93`  
		Last Modified: Fri, 15 Aug 2025 16:58:43 GMT  
		Size: 73.4 MB (73365758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e96be58cc45f2ba927d34bdf0172d2b8d7377124a996d42e808fdf4cfa3b72`  
		Last Modified: Fri, 15 Aug 2025 16:58:40 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98997d85e5d6da9c6d5dbf443b23fdcf0669368bd779025a5a1aa111a07e05f`  
		Last Modified: Fri, 15 Aug 2025 16:58:41 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2561dd56ac33c571b7b332395ece35ab92caa03f3829fa1196b1c368651cdbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b4eadb528c844dd226ae97105b841aa3bdec59d3be2ebd796fec7b00c04d54`

```dockerfile
```

-	Layers:
	-	`sha256:40af3552a2a3f4340d8e17e4d4daabf005c1c861aa2e8c1c1bb700cbcaeed15d`  
		Last Modified: Fri, 15 Aug 2025 18:20:22 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9a1c3998552633081142f8c46765d5f54144dbfa64f3433e87faddf2c883d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3709c2147eee9862efa2559144884bb8f59697f031c38c5f4e2fd36d829454e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5273443b55588922d029ea0a105bcef20161f7347f7723a8a2bf00ba5409c29`  
		Last Modified: Fri, 15 Aug 2025 18:20:52 GMT  
		Size: 79.1 MB (79115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5306d254fb0902aa4460d62f07845d4308e97c4f36214af53ad59455348b0`  
		Last Modified: Fri, 15 Aug 2025 17:27:23 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd7e5a4c259b0e2da55fdcc2a951ff2d4e57059a085970ba0a2a457820011b`  
		Last Modified: Fri, 15 Aug 2025 17:27:22 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:805ac3dbf45f6e2a1dbf9817a7b6a69e3226fdb19a16bb57330437319a30c730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9395e2b144bc8f7bc98fe149d18657a2e7b81ca6069c270aa4bd292983f413c`

```dockerfile
```

-	Layers:
	-	`sha256:817b6ca8afcbee4bba4d42bd3193dce131fa0fee46f80e1ba8c59a36877f5c1c`  
		Last Modified: Fri, 15 Aug 2025 18:20:26 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:4013273c17e4d73d0fff79e87e82d992487316c0462b023c2127b71d02b30ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76633537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d930a8ffe8c5620edda4a5ae4083beca22509b76dcca3f020352b803f9fa06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace93df466c17cd7ca7913c595aa0c794ea5fbd619f8289dcc0542b678139a1`  
		Last Modified: Fri, 15 Aug 2025 17:15:37 GMT  
		Size: 72.9 MB (72904365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98130a78b774a02fd26aae942aa7184d419e13cb2f08db2862a314215672524b`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9bc2376dfa75b485a5fcf0d9ffc4339b721217e78d0301c550afd8852dd93c`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b782e164fdc8b81adc6e74b39ae3b241c8a92987d16b383bc97a03b90d718e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230eaceef94b90468bf978df0fa292d7206e25542088ae0d930c0646ae9d272`

```dockerfile
```

-	Layers:
	-	`sha256:3cf726d2f7ef3fe6dc191ab3cfc4480ee577512d43c5c480b633013e45b4c749`  
		Last Modified: Fri, 15 Aug 2025 18:20:29 GMT  
		Size: 19.5 KB (19518 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.2-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:be77e8e657b601fa610f69d3c57c0d2477b9b7114b173dde5602654fd5d0416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89093a7ecc822c5b6def0853f54aee46c86cd4eb988f9c443e962fb9f0254f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b4cd4d200db742fc36965160bffa32a4266c50fe01a3a3098c5dd0c6f6ca6`  
		Last Modified: Fri, 15 Aug 2025 17:00:11 GMT  
		Size: 67.6 MB (67637480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd6b2622d0e954a05bede36e6c5572d4003aaca0a717adbcafc33fe4b9de7f`  
		Last Modified: Fri, 15 Aug 2025 17:00:06 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671b8de9982d6140e072fc678c363fb0760ca978dcfdcd4721579178cf7402e`  
		Last Modified: Fri, 15 Aug 2025 17:00:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.2-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4d661ac5f10739ea3990846451b229f77886a428fb934502f7809c628bbe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e5a16b6b5c9085598ef0af0b1290c2dee11db9794440119a10ed5d01fcec2`

```dockerfile
```

-	Layers:
	-	`sha256:c3364ad35a3f174f668207d29078228dc7d165a94b113fdb93703a0b7fa2b1a9`  
		Last Modified: Fri, 15 Aug 2025 18:20:32 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:11f468c0fac3c1c019ed680d37f905a4e97cf4d87d562202ed1ed6dc3054d7c6
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

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:7035c20e4805ab5f70599ef1e4057a1aa57ad7ae2d50f8409a93867f1cae4e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80505421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801bc1bb3b98d83d0802e4e829cc1218ea8134d53b4f06104d9f13978c59f0b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55297ffdb439992b8f725e1abee5cfb1f41f3c26beabd7e2bbb004029148296`  
		Last Modified: Fri, 15 Aug 2025 16:56:50 GMT  
		Size: 76.7 MB (76703672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bd86dfee1e73c6276ee94e788dc89ba827a83d22f4454a2011064fc9f82f4`  
		Last Modified: Fri, 15 Aug 2025 16:56:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539ddb67860c1bfec8f0ac73d49a345cdc44ba46ab1b6da9ef818f68cb290cc`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fff050818c236d2652dff618185a1b092aa7b86c042cf9dc46eb0c5ecc422843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb200068daf0e7aa4cc2e7d0f920c1c9b766b6f86e7ef8224f9c40022498079a`

```dockerfile
```

-	Layers:
	-	`sha256:b233189ccdc4fd3796925be1bb23d5c8269cefe12c4b7b0d123c7f36ffdf4156`  
		Last Modified: Fri, 15 Aug 2025 18:20:16 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9e81fcdb8ea18f49dac62d0e6f2395e6c5d1ebe5b537c2343ebbcdb3dd487397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62515065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9411aaf5f3dbef0e91342c29cf7d595ce30ee60f41d66e3fff2a369f4b1d8dfe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c6c5dcb5b4ac9ad073457a12700618c82623de85fb82f2d5fb326bca6a600`  
		Last Modified: Fri, 15 Aug 2025 16:59:02 GMT  
		Size: 59.3 MB (59293972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d82b3db827a281bb380ace01fc619eaa48d752c82e2fd376a28c752f1465ff5`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97cd2adc93836662f8319b7754daac32766095945bbbd68c407d62f8b7e1d98`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18353cb316e339f32e46a86e9a14cc92c68611618f1d0e7e409c14d87efa920b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fe86f4fcf0d2a0df26272c5ad8251508207e05b0fa78c65a4c02e77d0a1e9b`

```dockerfile
```

-	Layers:
	-	`sha256:eca07e957d3e688c6caee11f6b3e4e3efd6d17f0fbb83518fd0f96c10962a9e5`  
		Last Modified: Fri, 15 Aug 2025 18:20:19 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d6df66a151a86aa3c614afa6279d5bea14710a86ce3dfab839160b94d1e80ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77498564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053598a7edda72857a2903a0b0371938657afa3a81079b4cfae7a9555359b01`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34fadec23958052f927e36d3e2fa9dd9b9ce78567638099bc0d9334feb4d93`  
		Last Modified: Fri, 15 Aug 2025 16:58:43 GMT  
		Size: 73.4 MB (73365758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e96be58cc45f2ba927d34bdf0172d2b8d7377124a996d42e808fdf4cfa3b72`  
		Last Modified: Fri, 15 Aug 2025 16:58:40 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98997d85e5d6da9c6d5dbf443b23fdcf0669368bd779025a5a1aa111a07e05f`  
		Last Modified: Fri, 15 Aug 2025 16:58:41 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2561dd56ac33c571b7b332395ece35ab92caa03f3829fa1196b1c368651cdbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b4eadb528c844dd226ae97105b841aa3bdec59d3be2ebd796fec7b00c04d54`

```dockerfile
```

-	Layers:
	-	`sha256:40af3552a2a3f4340d8e17e4d4daabf005c1c861aa2e8c1c1bb700cbcaeed15d`  
		Last Modified: Fri, 15 Aug 2025 18:20:22 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:9a1c3998552633081142f8c46765d5f54144dbfa64f3433e87faddf2c883d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3709c2147eee9862efa2559144884bb8f59697f031c38c5f4e2fd36d829454e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5273443b55588922d029ea0a105bcef20161f7347f7723a8a2bf00ba5409c29`  
		Last Modified: Fri, 15 Aug 2025 18:20:52 GMT  
		Size: 79.1 MB (79115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5306d254fb0902aa4460d62f07845d4308e97c4f36214af53ad59455348b0`  
		Last Modified: Fri, 15 Aug 2025 17:27:23 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd7e5a4c259b0e2da55fdcc2a951ff2d4e57059a085970ba0a2a457820011b`  
		Last Modified: Fri, 15 Aug 2025 17:27:22 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:805ac3dbf45f6e2a1dbf9817a7b6a69e3226fdb19a16bb57330437319a30c730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9395e2b144bc8f7bc98fe149d18657a2e7b81ca6069c270aa4bd292983f413c`

```dockerfile
```

-	Layers:
	-	`sha256:817b6ca8afcbee4bba4d42bd3193dce131fa0fee46f80e1ba8c59a36877f5c1c`  
		Last Modified: Fri, 15 Aug 2025 18:20:26 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:4013273c17e4d73d0fff79e87e82d992487316c0462b023c2127b71d02b30ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76633537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d930a8ffe8c5620edda4a5ae4083beca22509b76dcca3f020352b803f9fa06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace93df466c17cd7ca7913c595aa0c794ea5fbd619f8289dcc0542b678139a1`  
		Last Modified: Fri, 15 Aug 2025 17:15:37 GMT  
		Size: 72.9 MB (72904365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98130a78b774a02fd26aae942aa7184d419e13cb2f08db2862a314215672524b`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9bc2376dfa75b485a5fcf0d9ffc4339b721217e78d0301c550afd8852dd93c`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b782e164fdc8b81adc6e74b39ae3b241c8a92987d16b383bc97a03b90d718e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230eaceef94b90468bf978df0fa292d7206e25542088ae0d930c0646ae9d272`

```dockerfile
```

-	Layers:
	-	`sha256:3cf726d2f7ef3fe6dc191ab3cfc4480ee577512d43c5c480b633013e45b4c749`  
		Last Modified: Fri, 15 Aug 2025 18:20:29 GMT  
		Size: 19.5 KB (19518 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:be77e8e657b601fa610f69d3c57c0d2477b9b7114b173dde5602654fd5d0416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89093a7ecc822c5b6def0853f54aee46c86cd4eb988f9c443e962fb9f0254f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b4cd4d200db742fc36965160bffa32a4266c50fe01a3a3098c5dd0c6f6ca6`  
		Last Modified: Fri, 15 Aug 2025 17:00:11 GMT  
		Size: 67.6 MB (67637480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd6b2622d0e954a05bede36e6c5572d4003aaca0a717adbcafc33fe4b9de7f`  
		Last Modified: Fri, 15 Aug 2025 17:00:06 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671b8de9982d6140e072fc678c363fb0760ca978dcfdcd4721579178cf7402e`  
		Last Modified: Fri, 15 Aug 2025 17:00:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4d661ac5f10739ea3990846451b229f77886a428fb934502f7809c628bbe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e5a16b6b5c9085598ef0af0b1290c2dee11db9794440119a10ed5d01fcec2`

```dockerfile
```

-	Layers:
	-	`sha256:c3364ad35a3f174f668207d29078228dc7d165a94b113fdb93703a0b7fa2b1a9`  
		Last Modified: Fri, 15 Aug 2025 18:20:32 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:83ca6fecb7781cf39d4489bad0d357d20a8edb943f5563b90ff46d94360f4ff2
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
$ docker pull varnish@sha256:fedfa20758d2651daf48ce3ae0c252539ec834fb1d8371335b8f13538c3d00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110106279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f281d5b0ed5e1cde6a33baf7c1a3f71055bd16d781940ec42a1a6be11bca5144`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767674a186da8285836153cb726409d4112a4a80fc976127bdf22c5df07a342`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 81.9 MB (81873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a35607832b0b15801f55356a07a24586b93213ef9a8d0c65fddc881463143`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddb218959aa0785586687d3d0aec6ce87943c57d054025007ae3f5f5780c5e`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:0e470651a8e0394799e7bbdf63d667730f87b8031f5db0a6d6dcfcc9aab04caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9b00d45d0fad1c56cab3e0d94f609b0838c8cd95edbd9e43910024dab3c76`

```dockerfile
```

-	Layers:
	-	`sha256:093b8a36638c67c6ebd86a569d5a9e880125463b6121e13cb842711c247e53df`  
		Last Modified: Fri, 15 Aug 2025 18:20:01 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6ef60b34629736d2141c8fb33ab6c2ea3a6a24b49a8cd2734b5c616daf0b8ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82361579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65f47712081b446c96886e6775c5643a2e8b77b1f93bafdc4d9060c488ae3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865acd02bf9c4f607ff081eacbcc80167f492e47029b6f33665a0092132885a`  
		Last Modified: Fri, 15 Aug 2025 16:57:09 GMT  
		Size: 58.4 MB (58420605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a9cb9947510c533811bb4f8ea48b8875ecdfcd746a0059cfb266744b2edb6`  
		Last Modified: Fri, 15 Aug 2025 16:57:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829b90f4f1f7509e840ecadd5046ff17ad077e9fffa3d6045fdd90d2b67b3ec`  
		Last Modified: Fri, 15 Aug 2025 16:57:05 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:5a95c4e9bdbda53ac19a4f7eb2fc7871c27bc54ec62f465520f9fed03f72c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ad9b4ae87f0700a77508ce6db54194c580d23dd71847fd987a3c2785c4571`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcf08c3380eaf1388cd59017438b8bfecd643cca66768e2856226c4b8100ce`  
		Last Modified: Fri, 15 Aug 2025 18:20:04 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c022a0ff5f7d30d8d65cdd3aad6a97f02e4d2bf8b551977c74d3e6784a78db30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9ba230852531c6b2deb4e5aebc846e12855d713a6f1daadb2367d71cd98992`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121caf58da77aa0443a2496d57c85ea79d8e1df2405a26b8d5e3673b479bf20`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 76.5 MB (76538135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec5280a3b9e492d66687c59a64df4f0f155ba5207db69037007ae5fde08120`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37110db52b9ecad7c7a879bb96852fe0ef35b0ece8dd3887a49bec4d0dfc3f3b`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:751a4801d5a9c5f699faad34be2f5905b06088ed10bf52f8b0b80ca728645a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664d38510adf7bbc0020d7dca45643c6126b6c65e459171cc4d00fe610eb1d2`

```dockerfile
```

-	Layers:
	-	`sha256:cf2d904d3d707278b34f5a4903707327e72e00baf0ae5df1a13efedb5d611426`  
		Last Modified: Fri, 15 Aug 2025 18:20:08 GMT  
		Size: 19.6 KB (19572 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:643e67a2f50b57bca50e83839f7f8b91b3c47588dd396769ede34e6db05e44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107508252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db414121d0e199a39b26554aef75af674c08942370d3c88386de0e1d008c1572`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a29dc117e0a7cf8a15e635b05ccf4d12c7a1ee6067cf3f182e71f264226655`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 78.3 MB (78293602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d90c530a68e0fbb406e32d98113522350b1170c276aaa0c300ec0cd5d34471`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020470a039d54dd250c2e33a0b7ad201a5a7dde161b96dd8aa20f54f65eb06d4`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:e403282207a41140505699aa134579847e5933b7c004aed9a357a12333a68bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c959bbaebf235be5668c87882884c538a7ba91403725fa4595ae53166076fbd`

```dockerfile
```

-	Layers:
	-	`sha256:9670f5aac7a9527cbdff76983554c8c1405a95db2b3b9ce78a62e32be01562b5`  
		Last Modified: Fri, 15 Aug 2025 18:20:11 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:5d63d6d9b3a816d335ab85a7fd3c24f078e8661c94d90f82cebdb65328894de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112125451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855097713d44be414c5475db87bcaa3807ac765b8529db689eff325ef52a983`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063bcd1ca526e732f14ddda8346106790e36b532d8f7ebbd7939f1f3390c975b`  
		Last Modified: Fri, 15 Aug 2025 17:00:10 GMT  
		Size: 80.0 MB (80049983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71734c96c8bc5b7e443557665eeda472a075a5cd5a0ac09e3b768ccbda14da8`  
		Last Modified: Fri, 15 Aug 2025 17:00:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b495f9c9889d394cacb9be69d494dc4f799f756dd6b652c7771f56bb6a8f82`  
		Last Modified: Fri, 15 Aug 2025 17:00:05 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:85986ce2cb4509cb6fa45a8f3c09981811c4036abad32fb472dd68250e65163a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dffec5d24b702fc55c635da910ac3d0da72d6da380f0d1e227dc9278646f6f`

```dockerfile
```

-	Layers:
	-	`sha256:a1646d6d4130c7e1c7b72eefc76d27ca9be0ce2306db99bbe68a55856ac896c3`  
		Last Modified: Fri, 15 Aug 2025 18:20:14 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:9141e45c7cd14117b58069fd59d4cc53c8badaeade8f9a536092c8143aa8e571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87911883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45dd74ae8f7452e7c68d37c305c66ffed0cac781869788d41e4882e352c37cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead03c3e8d7cd776db98c9f94e1610ca909dddfc22e62d793c6301988e7b4a97`  
		Last Modified: Fri, 15 Aug 2025 16:58:16 GMT  
		Size: 61.0 MB (61021999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f194092d9bc42b54e915dbd444d3b36e8d1e5343277b869e660e9ca0886c2b`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beefcc26fe8cb04b79d3ce2dbfeb6e61ce0c3553afc049dcf524ae6c44a25ab`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:4ec9d06a7ed84cb2369aa6497a334a6c5f94ed608f6bf9fd1c15e714d634b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f886ac06337c55578efdad672bd8221a76bfc5292462fb8f685c13c3a755c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f619217400a1c21827da3eb8bcf12dd75b9983fdfc57d3fa43c9fa87674f776`  
		Last Modified: Fri, 15 Aug 2025 18:20:17 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:11f468c0fac3c1c019ed680d37f905a4e97cf4d87d562202ed1ed6dc3054d7c6
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

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:7035c20e4805ab5f70599ef1e4057a1aa57ad7ae2d50f8409a93867f1cae4e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80505421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801bc1bb3b98d83d0802e4e829cc1218ea8134d53b4f06104d9f13978c59f0b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55297ffdb439992b8f725e1abee5cfb1f41f3c26beabd7e2bbb004029148296`  
		Last Modified: Fri, 15 Aug 2025 16:56:50 GMT  
		Size: 76.7 MB (76703672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bd86dfee1e73c6276ee94e788dc89ba827a83d22f4454a2011064fc9f82f4`  
		Last Modified: Fri, 15 Aug 2025 16:56:43 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539ddb67860c1bfec8f0ac73d49a345cdc44ba46ab1b6da9ef818f68cb290cc`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fff050818c236d2652dff618185a1b092aa7b86c042cf9dc46eb0c5ecc422843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb200068daf0e7aa4cc2e7d0f920c1c9b766b6f86e7ef8224f9c40022498079a`

```dockerfile
```

-	Layers:
	-	`sha256:b233189ccdc4fd3796925be1bb23d5c8269cefe12c4b7b0d123c7f36ffdf4156`  
		Last Modified: Fri, 15 Aug 2025 18:20:16 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:9e81fcdb8ea18f49dac62d0e6f2395e6c5d1ebe5b537c2343ebbcdb3dd487397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62515065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9411aaf5f3dbef0e91342c29cf7d595ce30ee60f41d66e3fff2a369f4b1d8dfe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c6c5dcb5b4ac9ad073457a12700618c82623de85fb82f2d5fb326bca6a600`  
		Last Modified: Fri, 15 Aug 2025 16:59:02 GMT  
		Size: 59.3 MB (59293972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d82b3db827a281bb380ace01fc619eaa48d752c82e2fd376a28c752f1465ff5`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97cd2adc93836662f8319b7754daac32766095945bbbd68c407d62f8b7e1d98`  
		Last Modified: Fri, 15 Aug 2025 16:58:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18353cb316e339f32e46a86e9a14cc92c68611618f1d0e7e409c14d87efa920b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fe86f4fcf0d2a0df26272c5ad8251508207e05b0fa78c65a4c02e77d0a1e9b`

```dockerfile
```

-	Layers:
	-	`sha256:eca07e957d3e688c6caee11f6b3e4e3efd6d17f0fbb83518fd0f96c10962a9e5`  
		Last Modified: Fri, 15 Aug 2025 18:20:19 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d6df66a151a86aa3c614afa6279d5bea14710a86ce3dfab839160b94d1e80ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77498564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053598a7edda72857a2903a0b0371938657afa3a81079b4cfae7a9555359b01`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34fadec23958052f927e36d3e2fa9dd9b9ce78567638099bc0d9334feb4d93`  
		Last Modified: Fri, 15 Aug 2025 16:58:43 GMT  
		Size: 73.4 MB (73365758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e96be58cc45f2ba927d34bdf0172d2b8d7377124a996d42e808fdf4cfa3b72`  
		Last Modified: Fri, 15 Aug 2025 16:58:40 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98997d85e5d6da9c6d5dbf443b23fdcf0669368bd779025a5a1aa111a07e05f`  
		Last Modified: Fri, 15 Aug 2025 16:58:41 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2561dd56ac33c571b7b332395ece35ab92caa03f3829fa1196b1c368651cdbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b4eadb528c844dd226ae97105b841aa3bdec59d3be2ebd796fec7b00c04d54`

```dockerfile
```

-	Layers:
	-	`sha256:40af3552a2a3f4340d8e17e4d4daabf005c1c861aa2e8c1c1bb700cbcaeed15d`  
		Last Modified: Fri, 15 Aug 2025 18:20:22 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9a1c3998552633081142f8c46765d5f54144dbfa64f3433e87faddf2c883d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82732803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3709c2147eee9862efa2559144884bb8f59697f031c38c5f4e2fd36d829454e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5273443b55588922d029ea0a105bcef20161f7347f7723a8a2bf00ba5409c29`  
		Last Modified: Fri, 15 Aug 2025 18:20:52 GMT  
		Size: 79.1 MB (79115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5306d254fb0902aa4460d62f07845d4308e97c4f36214af53ad59455348b0`  
		Last Modified: Fri, 15 Aug 2025 17:27:23 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd7e5a4c259b0e2da55fdcc2a951ff2d4e57059a085970ba0a2a457820011b`  
		Last Modified: Fri, 15 Aug 2025 17:27:22 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:805ac3dbf45f6e2a1dbf9817a7b6a69e3226fdb19a16bb57330437319a30c730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9395e2b144bc8f7bc98fe149d18657a2e7b81ca6069c270aa4bd292983f413c`

```dockerfile
```

-	Layers:
	-	`sha256:817b6ca8afcbee4bba4d42bd3193dce131fa0fee46f80e1ba8c59a36877f5c1c`  
		Last Modified: Fri, 15 Aug 2025 18:20:26 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:4013273c17e4d73d0fff79e87e82d992487316c0462b023c2127b71d02b30ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76633537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d930a8ffe8c5620edda4a5ae4083beca22509b76dcca3f020352b803f9fa06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace93df466c17cd7ca7913c595aa0c794ea5fbd619f8289dcc0542b678139a1`  
		Last Modified: Fri, 15 Aug 2025 17:15:37 GMT  
		Size: 72.9 MB (72904365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98130a78b774a02fd26aae942aa7184d419e13cb2f08db2862a314215672524b`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9bc2376dfa75b485a5fcf0d9ffc4339b721217e78d0301c550afd8852dd93c`  
		Last Modified: Fri, 15 Aug 2025 17:15:29 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b782e164fdc8b81adc6e74b39ae3b241c8a92987d16b383bc97a03b90d718e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230eaceef94b90468bf978df0fa292d7206e25542088ae0d930c0646ae9d272`

```dockerfile
```

-	Layers:
	-	`sha256:3cf726d2f7ef3fe6dc191ab3cfc4480ee577512d43c5c480b633013e45b4c749`  
		Last Modified: Fri, 15 Aug 2025 18:20:29 GMT  
		Size: 19.5 KB (19518 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:be77e8e657b601fa610f69d3c57c0d2477b9b7114b173dde5602654fd5d0416c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89093a7ecc822c5b6def0853f54aee46c86cd4eb988f9c443e962fb9f0254f6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b4cd4d200db742fc36965160bffa32a4266c50fe01a3a3098c5dd0c6f6ca6`  
		Last Modified: Fri, 15 Aug 2025 17:00:11 GMT  
		Size: 67.6 MB (67637480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd6b2622d0e954a05bede36e6c5572d4003aaca0a717adbcafc33fe4b9de7f`  
		Last Modified: Fri, 15 Aug 2025 17:00:06 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671b8de9982d6140e072fc678c363fb0760ca978dcfdcd4721579178cf7402e`  
		Last Modified: Fri, 15 Aug 2025 17:00:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4d661ac5f10739ea3990846451b229f77886a428fb934502f7809c628bbe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e5a16b6b5c9085598ef0af0b1290c2dee11db9794440119a10ed5d01fcec2`

```dockerfile
```

-	Layers:
	-	`sha256:c3364ad35a3f174f668207d29078228dc7d165a94b113fdb93703a0b7fa2b1a9`  
		Last Modified: Fri, 15 Aug 2025 18:20:32 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:83ca6fecb7781cf39d4489bad0d357d20a8edb943f5563b90ff46d94360f4ff2
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
$ docker pull varnish@sha256:fedfa20758d2651daf48ce3ae0c252539ec834fb1d8371335b8f13538c3d00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110106279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f281d5b0ed5e1cde6a33baf7c1a3f71055bd16d781940ec42a1a6be11bca5144`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767674a186da8285836153cb726409d4112a4a80fc976127bdf22c5df07a342`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 81.9 MB (81873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a35607832b0b15801f55356a07a24586b93213ef9a8d0c65fddc881463143`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ddb218959aa0785586687d3d0aec6ce87943c57d054025007ae3f5f5780c5e`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:0e470651a8e0394799e7bbdf63d667730f87b8031f5db0a6d6dcfcc9aab04caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9b00d45d0fad1c56cab3e0d94f609b0838c8cd95edbd9e43910024dab3c76`

```dockerfile
```

-	Layers:
	-	`sha256:093b8a36638c67c6ebd86a569d5a9e880125463b6121e13cb842711c247e53df`  
		Last Modified: Fri, 15 Aug 2025 18:20:01 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6ef60b34629736d2141c8fb33ab6c2ea3a6a24b49a8cd2734b5c616daf0b8ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82361579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65f47712081b446c96886e6775c5643a2e8b77b1f93bafdc4d9060c488ae3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865acd02bf9c4f607ff081eacbcc80167f492e47029b6f33665a0092132885a`  
		Last Modified: Fri, 15 Aug 2025 16:57:09 GMT  
		Size: 58.4 MB (58420605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a9cb9947510c533811bb4f8ea48b8875ecdfcd746a0059cfb266744b2edb6`  
		Last Modified: Fri, 15 Aug 2025 16:57:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829b90f4f1f7509e840ecadd5046ff17ad077e9fffa3d6045fdd90d2b67b3ec`  
		Last Modified: Fri, 15 Aug 2025 16:57:05 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:5a95c4e9bdbda53ac19a4f7eb2fc7871c27bc54ec62f465520f9fed03f72c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ad9b4ae87f0700a77508ce6db54194c580d23dd71847fd987a3c2785c4571`

```dockerfile
```

-	Layers:
	-	`sha256:4dbcf08c3380eaf1388cd59017438b8bfecd643cca66768e2856226c4b8100ce`  
		Last Modified: Fri, 15 Aug 2025 18:20:04 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c022a0ff5f7d30d8d65cdd3aad6a97f02e4d2bf8b551977c74d3e6784a78db30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9ba230852531c6b2deb4e5aebc846e12855d713a6f1daadb2367d71cd98992`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7121caf58da77aa0443a2496d57c85ea79d8e1df2405a26b8d5e3673b479bf20`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 76.5 MB (76538135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec5280a3b9e492d66687c59a64df4f0f155ba5207db69037007ae5fde08120`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37110db52b9ecad7c7a879bb96852fe0ef35b0ece8dd3887a49bec4d0dfc3f3b`  
		Last Modified: Fri, 15 Aug 2025 16:57:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:751a4801d5a9c5f699faad34be2f5905b06088ed10bf52f8b0b80ca728645a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664d38510adf7bbc0020d7dca45643c6126b6c65e459171cc4d00fe610eb1d2`

```dockerfile
```

-	Layers:
	-	`sha256:cf2d904d3d707278b34f5a4903707327e72e00baf0ae5df1a13efedb5d611426`  
		Last Modified: Fri, 15 Aug 2025 18:20:08 GMT  
		Size: 19.6 KB (19572 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:643e67a2f50b57bca50e83839f7f8b91b3c47588dd396769ede34e6db05e44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107508252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db414121d0e199a39b26554aef75af674c08942370d3c88386de0e1d008c1572`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a29dc117e0a7cf8a15e635b05ccf4d12c7a1ee6067cf3f182e71f264226655`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 78.3 MB (78293602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d90c530a68e0fbb406e32d98113522350b1170c276aaa0c300ec0cd5d34471`  
		Last Modified: Fri, 15 Aug 2025 16:57:39 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020470a039d54dd250c2e33a0b7ad201a5a7dde161b96dd8aa20f54f65eb06d4`  
		Last Modified: Fri, 15 Aug 2025 16:57:41 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:e403282207a41140505699aa134579847e5933b7c004aed9a357a12333a68bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c959bbaebf235be5668c87882884c538a7ba91403725fa4595ae53166076fbd`

```dockerfile
```

-	Layers:
	-	`sha256:9670f5aac7a9527cbdff76983554c8c1405a95db2b3b9ce78a62e32be01562b5`  
		Last Modified: Fri, 15 Aug 2025 18:20:11 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:5d63d6d9b3a816d335ab85a7fd3c24f078e8661c94d90f82cebdb65328894de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112125451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855097713d44be414c5475db87bcaa3807ac765b8529db689eff325ef52a983`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063bcd1ca526e732f14ddda8346106790e36b532d8f7ebbd7939f1f3390c975b`  
		Last Modified: Fri, 15 Aug 2025 17:00:10 GMT  
		Size: 80.0 MB (80049983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71734c96c8bc5b7e443557665eeda472a075a5cd5a0ac09e3b768ccbda14da8`  
		Last Modified: Fri, 15 Aug 2025 17:00:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b495f9c9889d394cacb9be69d494dc4f799f756dd6b652c7771f56bb6a8f82`  
		Last Modified: Fri, 15 Aug 2025 17:00:05 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:85986ce2cb4509cb6fa45a8f3c09981811c4036abad32fb472dd68250e65163a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dffec5d24b702fc55c635da910ac3d0da72d6da380f0d1e227dc9278646f6f`

```dockerfile
```

-	Layers:
	-	`sha256:a1646d6d4130c7e1c7b72eefc76d27ca9be0ce2306db99bbe68a55856ac896c3`  
		Last Modified: Fri, 15 Aug 2025 18:20:14 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:9141e45c7cd14117b58069fd59d4cc53c8badaeade8f9a536092c8143aa8e571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87911883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45dd74ae8f7452e7c68d37c305c66ffed0cac781869788d41e4882e352c37cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.7.2
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.2 DIST_SHA512=7a063fa26c01abef3f1c04adaf1a07eb8ebb3d7631f4c797fb4082c75d9133a1e830c5fbbf7f36cc921d502dcfbb36e93ef1cd46e65cf1885efcb740f86da8ac VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead03c3e8d7cd776db98c9f94e1610ca909dddfc22e62d793c6301988e7b4a97`  
		Last Modified: Fri, 15 Aug 2025 16:58:16 GMT  
		Size: 61.0 MB (61021999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f194092d9bc42b54e915dbd444d3b36e8d1e5343277b869e660e9ca0886c2b`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beefcc26fe8cb04b79d3ce2dbfeb6e61ce0c3553afc049dcf524ae6c44a25ab`  
		Last Modified: Fri, 15 Aug 2025 16:58:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:4ec9d06a7ed84cb2369aa6497a334a6c5f94ed608f6bf9fd1c15e714d634b2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f886ac06337c55578efdad672bd8221a76bfc5292462fb8f685c13c3a755c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f619217400a1c21827da3eb8bcf12dd75b9983fdfc57d3fa43c9fa87674f776`  
		Last Modified: Fri, 15 Aug 2025 18:20:17 GMT  
		Size: 19.5 KB (19456 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:55ac9db07a2b148fa275604f15a9b94f26445c54e11e1701f9ffe9729616ee37
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
$ docker pull varnish@sha256:a1fb2f20c12438ef482bf8149aece9528fdd8b24b6343ffa182a843889d7c2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109935364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a4d0525acdefa194b1cc9c28c9af7c752cc3cac711727419f40e73fa7fc387`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09267f7e5a383c22b01ad0bf5b02384b7345434b494f8a60bc90cdfb66934070`  
		Last Modified: Fri, 15 Aug 2025 16:57:49 GMT  
		Size: 81.7 MB (81703064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6f128744545326a15166b51afb3e08827e5cf2afdb7f60b6ce1208e3e95d14`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6829a15a5bc04c257c64e3468ee5f3e0b43ff44a6eab0e3d7382967f444045`  
		Last Modified: Fri, 15 Aug 2025 16:57:35 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:c222ef3b761cd4101767ce05ce4b3e7c56239128bc44e89e672e855647aecfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0556654bf18f33829c58cf35fca961103727c4188d34ec864fd5202871997ec6`

```dockerfile
```

-	Layers:
	-	`sha256:49690a315c3e50f7eb6d14c4bef2ef21a322a1b4e5310dba968ac567847b216c`  
		Last Modified: Fri, 15 Aug 2025 18:20:31 GMT  
		Size: 18.9 KB (18871 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:2dde0e165d54e25b0e0a42fcd98da86647a66f3cb6b28156330959b50e764370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82185203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc70aba460a17488c1dcffa90c4ac199283b309d2c4e24f5ca0de078f1dc599b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c482092d910c7110f0605ae4db82097e5f488b42c827f8abe3baea139c9535a`  
		Last Modified: Fri, 15 Aug 2025 17:01:45 GMT  
		Size: 58.2 MB (58244224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a4c5dacace037dd116a534d3e2e6cf0061119c6b1c5418734ba783d7515ad`  
		Last Modified: Fri, 15 Aug 2025 17:01:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fd9c49bf7a0d3736d7214af56dfed1230f54a846dc3380c17540eee10dd1f2`  
		Last Modified: Fri, 15 Aug 2025 17:01:35 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:2b37a8c98eee509364d75ab8f563bde11976bfd70be7c499813659cbc2745ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b617b048a15b0acca175b3a678db24692ca8cfacf6796525c717a1c4654c3f5`

```dockerfile
```

-	Layers:
	-	`sha256:6eba3dcedecd35442cb775edd859623bab177e01b7febc0e98b174e0cd568939`  
		Last Modified: Fri, 15 Aug 2025 18:20:35 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8b7c11552292d531475f0d54463beae68da5bdf7d859eb1a83a47afb479f270a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104449591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fa7fde6ec1a84fba9665510b54fdb2994fb2735d988f99e5778aa3b42bf80b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd0936b3e7a1906e0dcd9f67846122080e0fa52bd067c4fb7fc279ae847d0c`  
		Last Modified: Fri, 15 Aug 2025 17:01:23 GMT  
		Size: 76.4 MB (76365546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21739974fa1f38fd215745094ac2db46becce16d34d034a3a2c3c8e62a0987ea`  
		Last Modified: Fri, 15 Aug 2025 17:01:16 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c890712c0af0dc42f3c1a1a7db2493a3c986de76bea5c7ee6ead7a2911a6f43b`  
		Last Modified: Fri, 15 Aug 2025 17:01:16 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e934bfe8943e75dbd1d6bcd8e27048c270da9c865168d9a88dbed68bf1c77328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b43d13e42577bd39579d32bbf27a9a995b8b310bb766e1358677b0c0d6688cd`

```dockerfile
```

-	Layers:
	-	`sha256:6a38d12aa59e268d53752119c2808a8922cf235d7335eaf0b0f450cd0afdfb93`  
		Last Modified: Fri, 15 Aug 2025 18:20:38 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:10a5db2b243687d760fa20c79999a7c632b4691793acc4dd1a5d95356d02db16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107339580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd50e7d7df3a4b515a1c8ae46a155d2c5bf426c62db280ca2fa8365071bca83`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c62e81843249b5cb46ac342e6453be1c2b9d3b959437306a9a077d403976b3`  
		Last Modified: Fri, 15 Aug 2025 16:57:46 GMT  
		Size: 78.1 MB (78124931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc091cc50d8ccb50f08b1eddff8c15d443ddee40df8eabcd21c594d5826f44f5`  
		Last Modified: Fri, 15 Aug 2025 16:57:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1922589f9b12760e939f8eb0c74c48a75dcaf00c702c049b7b360aa83c15288a`  
		Last Modified: Fri, 15 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:7ee892531be69de90be55946b0a76a0c6ddc8be3a38696bf99e733b2362a0f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec6abd510c3912a99835ec879a9914911d4495ac9f7d6063b3f7a036839c6a9`

```dockerfile
```

-	Layers:
	-	`sha256:9b42f2b3d67bc1dbd8f2ba77391f5a5562ae5eaf1da2f64250db6463a0ee8589`  
		Last Modified: Fri, 15 Aug 2025 18:20:41 GMT  
		Size: 18.8 KB (18844 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:d771d0a11e5cb044fb29e243105d0fbaab24c34f772c4e6161e5e6cc6e2aae36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111970696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7fbf7aea862f1ce5f5b6743855ca732d0f26f5bf013b2bab03fd7e6a722e56`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f128671fcf877380ff6584510acfe5b88b91f2658c3348c827730b222267a31`  
		Last Modified: Fri, 15 Aug 2025 17:21:02 GMT  
		Size: 79.9 MB (79895231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981a0080d7c508255eac372f3977fbeb18600432db4ca13c65d3a567527af707`  
		Last Modified: Fri, 15 Aug 2025 17:20:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8407d8692a211522d3327eafc25ce587b9c952337fd433bb34be66bbd2517b`  
		Last Modified: Fri, 15 Aug 2025 17:20:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:479a8356add5b245a038ab07bb03f40962d410e4cff3fe671f0c3c35c7c45c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d3f1bc54dacefb5e68e75b5ccd1a117df8d285362cc6e80737b2fa1efe994d`

```dockerfile
```

-	Layers:
	-	`sha256:08ec36e5441b3a6da7a97f757f3e01f7b9a3d321e129455be42b51382a74a2fc`  
		Last Modified: Fri, 15 Aug 2025 18:20:44 GMT  
		Size: 18.9 KB (18909 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:b42f11c5699d210935309a878e399a8123e82e28ff9753c2ade5c960aa5d7080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87740299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be0ad2520373e21bff38de538ae40b78fd68435c1fdc6f4a3a7acbbb6b1932a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eb726fb2e8bff58331cf376c5c7a5e8696a9d03c548971766e4d1cbeb15097`  
		Last Modified: Fri, 15 Aug 2025 17:03:06 GMT  
		Size: 60.9 MB (60850415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b6eba540f8219227bdcc54c0371204b3f3e02094a4c5a5ab53d8970c51f0f3`  
		Last Modified: Fri, 15 Aug 2025 17:02:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac740b1ffc0d320f134e48c4c99a02b78cfb4d5948a7df22a6866d238d1acace`  
		Last Modified: Fri, 15 Aug 2025 17:02:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:50a68b601ee2b9d22d4ea3e1451db8ff2fdbf0992d3c6ed06becf9ecd3d6d75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751bfecbd724e325e691d6c1a0716f9f5d6fa5a454980a62a1e9afa46aff0441`

```dockerfile
```

-	Layers:
	-	`sha256:b87c115665c3f7e88b3595825828f2bfd7c869b6b38da7ee1325abad95f30db1`  
		Last Modified: Fri, 15 Aug 2025 18:20:47 GMT  
		Size: 18.9 KB (18870 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:55182b60b8fdb5e3d7cde85507b1a8780e863c814ded7a044795cb1e3d1aaa62
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

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:2e28523af3ac62ce8f5df5f1f528566614755c5d894c54344910267bd3014915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80360313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beadf1b6133d1fb4e2ed6c98af3b2abe24491418b6463974072b0e660e4bd4c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68d422905e258b2c06abba33d7cac42168221aae0303a010a04f88ab2a23e55`  
		Last Modified: Fri, 15 Aug 2025 16:56:55 GMT  
		Size: 76.6 MB (76558565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85a4d5fc6a71c879deaaffde6d40e4a3760be40258c90c7d95a7fe88d79d83d`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3efcf70e77659dfca5f522a6ac025643e281dc719b7a6fbb9426e52547e3aa`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2f2c53f07fd781d6b92cde6bd8a0200ef8e46f8078da33daad6189adf566ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f6e344f9f5a29380d92ff128e32536769ed41f708a1f252ae37d52158098c`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a2d976a799d47c2d5fc2781e7b8b0fc7629e7f5255e105572a894d111c352`  
		Last Modified: Fri, 15 Aug 2025 18:20:48 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:379bab88ceec859e19e44981f502567af57036b8ff5a8c69a4b6a232ce630d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a3bb0cfd3e7e60866c632497e1ed49c3968ca3cf81914657a2587d5311bb90`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be65ae8220b17cebc4940557f2bbca478767709227469272b08f5ced5579884`  
		Last Modified: Fri, 15 Aug 2025 18:21:21 GMT  
		Size: 59.1 MB (59137869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb95b95fe2980a84518f818b4cb4edb91d42de110d0e72f16514ccb0e006797`  
		Last Modified: Fri, 15 Aug 2025 17:37:26 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86919752bd9d80fb2171c0558735ef137e8ddae97d261f939e8b2a627b5177`  
		Last Modified: Fri, 15 Aug 2025 17:37:26 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e48b51726d379095a17ac602baeedb7467118f85e0cc52f14ea3df8fd9527151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcab1367b7d94d5e25fbc2d6964558b907332f898b1b2fc98d669a379e1e827`

```dockerfile
```

-	Layers:
	-	`sha256:455ea1d61388ff00a462eef0e62d92f4b9bd1a3033652833b25971ad2b87b955`  
		Last Modified: Fri, 15 Aug 2025 18:20:51 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:01f30396ee7885727a37b05f4ceeb938e73272c8f89b31c54310fb83686707df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77352942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff942430636abfe637f6deb2253b3ba9195b9bd093f984e40e8f695771520335`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0973e7274fbb6bb2d79f5f57dfa272b575144ab267d6a557fdc4df744c0b74`  
		Last Modified: Fri, 15 Aug 2025 17:02:44 GMT  
		Size: 73.2 MB (73220136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65416659d0fee5f6390111a1ec275b5f477e16c962c32a015f9a1aefb7a4d6`  
		Last Modified: Fri, 15 Aug 2025 17:02:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f872359234a71fdbc0b46bae9130c45f63743ed2f5988bf0d976f1ebb1c81d6d`  
		Last Modified: Fri, 15 Aug 2025 17:02:39 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7022499599f7d49c6495b5860eb8fae5768054eb8c5f2ba91994c43a98eaf286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fa2a3c79d99a04a7c2f6b871415d4f46fb3b2ed016ab9845c9ca8cf1ee62ba`

```dockerfile
```

-	Layers:
	-	`sha256:1a816257add10eeb647349f6132d182818df3486dfbdc16ea6d187a87617d3b0`  
		Last Modified: Fri, 15 Aug 2025 18:20:54 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:8c954b7c4405960ec73f5b9499efa166879e3833b0f19d30fffbf5bc8687b718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82580620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f903a36f5ec669127c6300b7d209aaecff97df86bdab35c05a2759e8faa95`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15d6e5299710cb5dac41d28835746591e5c014d20c9f7f59e709acd8b6bfa9`  
		Last Modified: Fri, 15 Aug 2025 16:56:54 GMT  
		Size: 79.0 MB (78963559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6985a2ac50be822aabc113ad078cecb13cfdac13f050dc4d848af2bb863be`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2738232ef9048b3d2198553c94078c35c3411d9238481dc8a1612f81fb6461`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a7d4573bd79febe0431d5079c48652a8ee5ea0b7468744bdfcd7ba621eddb53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911f14009c07b52f51cbb0687d7be87cd14c2ece0eb64130467fde8faa6dc840`

```dockerfile
```

-	Layers:
	-	`sha256:c18a7c2a195c59ca73c6a808b6cdf7eec2d29d151a8a2a7ae533fb8536370a70`  
		Last Modified: Fri, 15 Aug 2025 18:20:58 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b5cc2effed9d3c96575813c9ae309e4960db421a496cf58e385b94ed61b4ac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76484344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08567c3f69380d78bfe7e2ef06e32db6111c54cc25650a124212b2d5449edd2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6adaf6b71bfb3b3d4d0ba7ed33358cd92e00982fe08244fba3852b9dd12ca`  
		Last Modified: Fri, 15 Aug 2025 17:08:01 GMT  
		Size: 72.8 MB (72755174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458b177cd2bd3f4be3d8851688aeb8c640756a34ae684c9b69edf5d151794f09`  
		Last Modified: Fri, 15 Aug 2025 17:07:58 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b90bc979cc22ae747545bdc0a3573ef5709d682e7698b78fd384b5c7d988b3`  
		Last Modified: Fri, 15 Aug 2025 17:07:58 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2dd7232cbb0c05ba7d9bdc08242f54049d0b87b3bce079343fb48221516a9188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a41a0d8ab9703a676ba00d7c43045fde0e751484dd3bce7bdede95d9d8bb20`

```dockerfile
```

-	Layers:
	-	`sha256:1d7949d6c0cde8823ab8ec84f441a8a4584c5a89230d42d8e3d52ca0aa77fcef`  
		Last Modified: Fri, 15 Aug 2025 18:21:01 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:418964a60a086568bf3c9e24c151fc6fdf49daca5770be03811a399f1629591d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71137048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec28ce9e35799416d5561fa764a0166f74b2242c440060cc18dcf2b605909cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=7.6.4
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 15 Aug 2025 11:36:20 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VSM_NOPID=1
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.4 DIST_SHA512=3af49e766bc9fe3686d859dce5b299b4caec07b18e91079f384f0a947bebed02ae9d9030f4a3f51b5c316e71ca07124ae83fbebcfe905b29ff9a285e6daea887 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
USER varnish
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f85783785f4a910b12b3142daf7b9792b10396fde68fd61c9942aacd69a210`  
		Last Modified: Fri, 15 Aug 2025 17:05:06 GMT  
		Size: 67.5 MB (67490017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e26276b94a3776f76510bb59649174ea49218dce0cb142ade303c1e895c76`  
		Last Modified: Fri, 15 Aug 2025 17:04:46 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1afe2786b0558220edbb297ad06dac559501792e8cdc14f08f15a51966f41`  
		Last Modified: Fri, 15 Aug 2025 17:04:46 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4adc40aa798e4122db270aee5f3769196a6c13585fcda05dcc5165073d9f3323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb03c38bf58b26da7e3da97acbb77b9256d2421857e9a3feff783b01427d630d`

```dockerfile
```

-	Layers:
	-	`sha256:e18057a42643b81492b6588dbbf5c71b2a3256d69d3055bc5be864b4d1ab7bb2`  
		Last Modified: Fri, 15 Aug 2025 18:21:05 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:508c568a36f190ac356251acbb738eff0d9e50f98753925761f01e94e2b6b824
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

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:4f205404369001e63bd78cb37c84db57e99eefc0102598dd9756ed74bd3b1d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103551015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205a2b1a1f5d3dd4eabcaf07fb315d5c006eb98f4c0dd4ecd1015901b826425a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b3030307e8a54c17da978aa122b40a64286d7dd94f9021c4dfe39d4eda81fd`  
		Last Modified: Fri, 15 Aug 2025 16:56:49 GMT  
		Size: 75.3 MB (75320004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087091d157f20b70b465cc1363850e48778034d11c403fa6c5375a6e9c7581b1`  
		Last Modified: Fri, 15 Aug 2025 16:56:41 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:6a3d52c00cea8a4782380fbe188167a6a64dc4516dd0584e5905e61c69d1efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239f662812bdbe99ba31e39373a27c94bdf60c9401fb1aa40a65163bb577588`

```dockerfile
```

-	Layers:
	-	`sha256:3105daaa0e7fbce636d5e26dfde9dc7e468ea3fec101c8ced4bc8bd3647a41b8`  
		Last Modified: Fri, 15 Aug 2025 18:19:40 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:63fb769bea28f1be50113c499f024710a06c6b691dda3f845e0c6ed61ae5d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75972675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545192084d1f68c292e6676630c61b0f4a703f5f749cf7b9b9af51d90755edb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4f5cdc2b29e6e9f7e366dab90d0d13fe6bb1e6936c47d9a7f28c78494b0a15`  
		Last Modified: Fri, 15 Aug 2025 17:05:40 GMT  
		Size: 52.0 MB (52032989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ad42f5a97af5a103fc53c0068a770844b25168bd89f510dd1208b539ec6d76`  
		Last Modified: Fri, 15 Aug 2025 17:05:34 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:250fd3b0d47cfd437f00fefcf0895fb71dc39ae74ca9354f6952d6128f69059b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3994e63f9a6a786cab6f39a88fcc39cf68615db7197fb977a0cde17607a0d`

```dockerfile
```

-	Layers:
	-	`sha256:3f1ae9bad7cc686af951d8f0988a09bde737235f52aa1242cdedea30e424432f`  
		Last Modified: Fri, 15 Aug 2025 18:19:43 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3d8591b4c8a49bb34772636c11837f394c0427644eb1bfa5760398b302cf1f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98372375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b103782bf675afb16ccb328ff82ca3fd0d13b7c41dab6166c43ed41a92e53b31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d4c5411a8a5191465e747e040f148e3e2954ffe4efc3b5e6df88a5197f7df9`  
		Last Modified: Fri, 15 Aug 2025 17:04:52 GMT  
		Size: 70.3 MB (70289618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c5a5db02a078d9b226d17d533ae6a4873897fb3e51fd16f5e2fec3a22de552`  
		Last Modified: Fri, 15 Aug 2025 17:04:45 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:3585cf5a7a99c879f94875ff1d9dda046ffb97aa31aad46c7e35370186653927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8a622ee63b17d5b8c7c01ad26a27c25b1c03d2eb5e4676f8d5c1a0512b2b38`

```dockerfile
```

-	Layers:
	-	`sha256:176774f0bf55f60639b47cccfa92496e9c88f4baa2bae7b2f29d35b71c9bfa13`  
		Last Modified: Fri, 15 Aug 2025 18:19:46 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:c1e45daaad2256afb1d92957408e28157149055d2890299abbd06dd7eac9a4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc42e044e9794a4e6b353970c333eb95173dbd6deb7983e4496934994375dbea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6c5110dee275f4bdc6a6440f5c4605e685665d32fdc0d9eac6395187e92e21`  
		Last Modified: Fri, 15 Aug 2025 16:56:52 GMT  
		Size: 71.8 MB (71798834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce5ced758f20dd5e228d5b673317afd748a1673753da7c6a676eea3fc2bd7`  
		Last Modified: Fri, 15 Aug 2025 16:56:45 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:cd4624282828006ad76c2c2cd6588452b66645c9688b342db848641294ab682b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba0bb4524ec66863a46f64a64abd4d1da26c235b266c8e25e21ad3325615df`

```dockerfile
```

-	Layers:
	-	`sha256:def37e74e38e4692944a7846f46cc443d74133538355871dde977f1b20a7e8ae`  
		Last Modified: Fri, 15 Aug 2025 18:19:50 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:59ca61d9c88cec3e2a850c09b44b62e9366743ac8b2a8f3f0f56fd7647549093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105453532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ececacc8625c0cf7ed467c2ea49c947f651a65b3cf6406577b361cb99d15f38f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140f2e5f7e62807eb83bf1d06d3de2b7ca8432c4a959eee34569191dc51fc57`  
		Last Modified: Fri, 15 Aug 2025 17:13:11 GMT  
		Size: 73.4 MB (73379358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6722af99a347451a061f526da91a19fcbe85026ad68115418e60c07dc9b91`  
		Last Modified: Fri, 15 Aug 2025 17:13:04 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:ca5e6fa34de326f0e638ec5ceaec95fc5b12363518101a227fb8b8cd5573e688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accc1929eb0e7d44f7aead289ecbe585947c71c34aeaadbc842633279d0c6690`

```dockerfile
```

-	Layers:
	-	`sha256:87e0a9ba0d00efa32d31b56794478a0fe0c596e0d6ae8c38d130ec41e83eaf25`  
		Last Modified: Fri, 15 Aug 2025 18:19:52 GMT  
		Size: 12.7 KB (12730 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:473b70ef10a50ce071860f7c79b3ad0fd20b97ca1326c17c989973a2b1c0e1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81338348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bed7f9db4a05ae7b0f9c6a03d049967991f6796f0a734186ace7d06b82dffe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 15 Aug 2025 11:36:20 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 15 Aug 2025 11:36:20 GMT
ARG VARNISH_VERSION=6.0.15
# Fri, 15 Aug 2025 11:36:20 GMT
ARG DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
# Fri, 15 Aug 2025 11:36:20 GMT
ENV VARNISH_SIZE=100M
# Fri, 15 Aug 2025 11:36:20 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.15 DIST_SHA512=70e87be7c12c1fe8696f74b7f8a94d0ef3b8c1fdab4ddee75b06493c9c82e6e9ce8d6115acb4071ee880ce827e261253b0c61b5cf296fa8a438f9ffa24814d4e
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
WORKDIR /etc/varnish
# Fri, 15 Aug 2025 11:36:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 15 Aug 2025 11:36:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 15 Aug 2025 11:36:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 15 Aug 2025 11:36:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70df0ff3df5e69e08e5b4b753ab705a5f7a7ccd7f9214d5dd81f48be05c515a8`  
		Last Modified: Fri, 15 Aug 2025 17:07:05 GMT  
		Size: 54.4 MB (54449756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe0f8eb19dd0db4199e2a97ba899a4da6e3274dcc34d2e879c85315f9d22924`  
		Last Modified: Fri, 15 Aug 2025 17:07:02 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:9af53eafac86b7f6351134d69f526deb3163438739a1bd002b592275ac7a7fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d666bc79cbdbe8e4256f9ce8af8739b6e5a406e78e33a4835d3e75471e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f5be1a6ced377aa9370dc51363ceba74a5599b107c3b84abe75dc345be4f83c5`  
		Last Modified: Fri, 15 Aug 2025 18:19:55 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json
