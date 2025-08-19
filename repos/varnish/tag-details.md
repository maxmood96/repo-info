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

### `varnish:7` - linux; amd64

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; arm variant v7

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; arm64 variant v8

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; 386

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; ppc64le

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; s390x

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

### `varnish:7` - unknown; unknown

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
$ docker pull varnish@sha256:22862d9143d6b1c489f434ce12640bfc4d7673d83423e221d28c3db291a313db
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
$ docker pull varnish@sha256:b092170cc8cb55549b1526dac8b8f64282f3e2669e58467c71c77ac73a58ff51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109946143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72ffe6810b784df3e44bddc8fec95bcaaf1425191ecb9b15623103105392442`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440cd84223df1ce32a4ecce96b18cd92436b79a32386a43d47021befaa35d9ca`  
		Last Modified: Mon, 18 Aug 2025 23:02:47 GMT  
		Size: 81.7 MB (81713848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe782b4816b6553b623cb27b82f2707908899ce8188699af63b33fd8e0c07c76`  
		Last Modified: Mon, 18 Aug 2025 23:02:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833de31c69510652b368756bc1516777d2fa5bb95467cd22b122645402d525e7`  
		Last Modified: Mon, 18 Aug 2025 23:02:43 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:c6933e8ef3c005edfad31453d9f6efb39183f962cfe08202e9d6717834628da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6341c78059c7be4fcae532f5a70ea56a5d3ce72ef20ed17f26c837a9f96f9086`

```dockerfile
```

-	Layers:
	-	`sha256:da89395ec937789492531a3f66e128f8a970f39adccfe3858f386eba3202aa35`  
		Last Modified: Tue, 19 Aug 2025 00:19:57 GMT  
		Size: 18.9 KB (18891 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

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

### `varnish:7.6` - unknown; unknown

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

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:57b58ac36e1117b974c1608fee9aa420043c0015270538237cbde85fb66f79bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104466921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae84b77d8db5444cad5daf9297597a4c0f2bc89cb48af7b35d28655c81b8a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66904f2fe198d1409d4d5b11a801d7c3c50b7addeb43a84322a068b404d2b`  
		Last Modified: Mon, 18 Aug 2025 23:04:56 GMT  
		Size: 76.4 MB (76382877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b87e4ebcc55ab78fbea549c0047e775d228e86a85afb389369517684db86c56`  
		Last Modified: Mon, 18 Aug 2025 23:04:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1062ff34d0d7890e63ea74a217ee3fb9f902a80beacf30f2f97a24d60bf22`  
		Last Modified: Mon, 18 Aug 2025 23:04:52 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:e1e8507a8a81163188b75f69bed4371b82f2dc8063695958b2cc943de3a1af5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e2b7f8978ed026596049adaf1fdf7b354e68147e6d0f0dafd39b6ac55f4db9`

```dockerfile
```

-	Layers:
	-	`sha256:126f0f6aeabeb1bd9d4ba14911fb0a71d6a5a3fa2a88419f0e4623416031f326`  
		Last Modified: Tue, 19 Aug 2025 00:20:04 GMT  
		Size: 19.0 KB (18983 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:67358cd862134c4c44836bfbdcf3fd3d55a9d6b4f8e192ac32c00b06175f98d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107373844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d79c4681c14e1c40f6e6d18cc36222e2dfde5934bbe356817ef4ce8dd5ccd37`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
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
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068d73f957a05a45d0a78f12295db7e93429b1d5e0095b2b746eead4629087a7`  
		Last Modified: Mon, 18 Aug 2025 23:02:46 GMT  
		Size: 78.2 MB (78159195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ca2311c7318efd7145d539dc5fba5f51f53a6593f6e486d627dcb98027caaf`  
		Last Modified: Mon, 18 Aug 2025 23:02:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb795850fc867113d69da2ea60da2d2ebc851ba8e8729c591165badcb66d98e`  
		Last Modified: Mon, 18 Aug 2025 23:02:37 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:fcb941b07afd3706ba5bca42861cc60ad0a767125d0592c309421ae6e459155c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22807049c2bbc575a18540bc0c27532aecbe84b6b122939b22bca86dc82e8a25`

```dockerfile
```

-	Layers:
	-	`sha256:f9b83c3b60b750a0738872fe5d85e5c12833307403148fc1d0c4aa49e85ffce1`  
		Last Modified: Tue, 19 Aug 2025 00:20:07 GMT  
		Size: 18.9 KB (18864 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:ccdcb7601062d3e85a322afee0803947d1e7bb150240c7703791df7e9fea4558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c59d3a3e361556d3458fe10eb466ae200ec0ca685b864059468abe6fc656631`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5dcd21108357c0c849635f3aca97e0e649ab2867b7fa1874ef0e73a5ba1f09`  
		Last Modified: Mon, 18 Aug 2025 23:09:08 GMT  
		Size: 79.9 MB (79901047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b381c74c88b922841cdfcef3d27c5768858212296b6725b703ce68e95a6e819`  
		Last Modified: Mon, 18 Aug 2025 23:08:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4c6c5ddc9fcf1628601e63e6226a35ce01359c83cfd9d1c015c4bb745e979`  
		Last Modified: Mon, 18 Aug 2025 23:08:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:5d151538c4529a61b5e38e137903d3184a9ac3bd6fe08b67ccda1f389ada0cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69907263d679a2c3acccfc36168c57c5d58cd27067848ce7c4336564f8be419`

```dockerfile
```

-	Layers:
	-	`sha256:d7400bccc5ebe6df4f853353ff842398d940a5fd19fb8af955d46ee8831f87b5`  
		Last Modified: Tue, 19 Aug 2025 00:20:11 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:c51e07bde0f4bc684535b99752d6c1ffe5227d4da853252488991a929abbe8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87765648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb92f010b81bf7b2a702f526012301fb366911747300b8edb612188effe6c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70b7e13106db60c770a8a12e8bc1f58e629360de9920a64ca753f4c1317affb`  
		Last Modified: Mon, 18 Aug 2025 23:52:17 GMT  
		Size: 60.9 MB (60875764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82e7dd3d2496d842018db7d80b4ed31c6d31ff4d54a03acfdd56b6941dc8de7`  
		Last Modified: Mon, 18 Aug 2025 23:52:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85340c5d7e5955c218bb662463169bbed0cba4111fd0196e82e956f85cdf304`  
		Last Modified: Mon, 18 Aug 2025 23:52:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4dc9ddcbf370be0b20fc67f0af250e87a02e8a0da612fd59adb0718babbfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd44cc4240ede6fbf63a1cd21c22570ef6d60d3795dd5d14da4a9d3559184b0`

```dockerfile
```

-	Layers:
	-	`sha256:730f509db0663bf93c9fc9e1251a7a8e7921a33d088738d5dd20ac7969a869c6`  
		Last Modified: Tue, 19 Aug 2025 00:20:14 GMT  
		Size: 18.9 KB (18890 bytes)  
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
$ docker pull varnish@sha256:22862d9143d6b1c489f434ce12640bfc4d7673d83423e221d28c3db291a313db
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
$ docker pull varnish@sha256:b092170cc8cb55549b1526dac8b8f64282f3e2669e58467c71c77ac73a58ff51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109946143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72ffe6810b784df3e44bddc8fec95bcaaf1425191ecb9b15623103105392442`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440cd84223df1ce32a4ecce96b18cd92436b79a32386a43d47021befaa35d9ca`  
		Last Modified: Mon, 18 Aug 2025 23:02:47 GMT  
		Size: 81.7 MB (81713848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe782b4816b6553b623cb27b82f2707908899ce8188699af63b33fd8e0c07c76`  
		Last Modified: Mon, 18 Aug 2025 23:02:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833de31c69510652b368756bc1516777d2fa5bb95467cd22b122645402d525e7`  
		Last Modified: Mon, 18 Aug 2025 23:02:43 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:c6933e8ef3c005edfad31453d9f6efb39183f962cfe08202e9d6717834628da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6341c78059c7be4fcae532f5a70ea56a5d3ce72ef20ed17f26c837a9f96f9086`

```dockerfile
```

-	Layers:
	-	`sha256:da89395ec937789492531a3f66e128f8a970f39adccfe3858f386eba3202aa35`  
		Last Modified: Tue, 19 Aug 2025 00:19:57 GMT  
		Size: 18.9 KB (18891 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; arm variant v7

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

### `varnish:7.6.4` - unknown; unknown

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

### `varnish:7.6.4` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:57b58ac36e1117b974c1608fee9aa420043c0015270538237cbde85fb66f79bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104466921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae84b77d8db5444cad5daf9297597a4c0f2bc89cb48af7b35d28655c81b8a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66904f2fe198d1409d4d5b11a801d7c3c50b7addeb43a84322a068b404d2b`  
		Last Modified: Mon, 18 Aug 2025 23:04:56 GMT  
		Size: 76.4 MB (76382877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b87e4ebcc55ab78fbea549c0047e775d228e86a85afb389369517684db86c56`  
		Last Modified: Mon, 18 Aug 2025 23:04:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1062ff34d0d7890e63ea74a217ee3fb9f902a80beacf30f2f97a24d60bf22`  
		Last Modified: Mon, 18 Aug 2025 23:04:52 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:e1e8507a8a81163188b75f69bed4371b82f2dc8063695958b2cc943de3a1af5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e2b7f8978ed026596049adaf1fdf7b354e68147e6d0f0dafd39b6ac55f4db9`

```dockerfile
```

-	Layers:
	-	`sha256:126f0f6aeabeb1bd9d4ba14911fb0a71d6a5a3fa2a88419f0e4623416031f326`  
		Last Modified: Tue, 19 Aug 2025 00:20:04 GMT  
		Size: 19.0 KB (18983 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; 386

```console
$ docker pull varnish@sha256:67358cd862134c4c44836bfbdcf3fd3d55a9d6b4f8e192ac32c00b06175f98d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107373844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d79c4681c14e1c40f6e6d18cc36222e2dfde5934bbe356817ef4ce8dd5ccd37`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
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
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068d73f957a05a45d0a78f12295db7e93429b1d5e0095b2b746eead4629087a7`  
		Last Modified: Mon, 18 Aug 2025 23:02:46 GMT  
		Size: 78.2 MB (78159195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ca2311c7318efd7145d539dc5fba5f51f53a6593f6e486d627dcb98027caaf`  
		Last Modified: Mon, 18 Aug 2025 23:02:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb795850fc867113d69da2ea60da2d2ebc851ba8e8729c591165badcb66d98e`  
		Last Modified: Mon, 18 Aug 2025 23:02:37 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:fcb941b07afd3706ba5bca42861cc60ad0a767125d0592c309421ae6e459155c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22807049c2bbc575a18540bc0c27532aecbe84b6b122939b22bca86dc82e8a25`

```dockerfile
```

-	Layers:
	-	`sha256:f9b83c3b60b750a0738872fe5d85e5c12833307403148fc1d0c4aa49e85ffce1`  
		Last Modified: Tue, 19 Aug 2025 00:20:07 GMT  
		Size: 18.9 KB (18864 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; ppc64le

```console
$ docker pull varnish@sha256:ccdcb7601062d3e85a322afee0803947d1e7bb150240c7703791df7e9fea4558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c59d3a3e361556d3458fe10eb466ae200ec0ca685b864059468abe6fc656631`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5dcd21108357c0c849635f3aca97e0e649ab2867b7fa1874ef0e73a5ba1f09`  
		Last Modified: Mon, 18 Aug 2025 23:09:08 GMT  
		Size: 79.9 MB (79901047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b381c74c88b922841cdfcef3d27c5768858212296b6725b703ce68e95a6e819`  
		Last Modified: Mon, 18 Aug 2025 23:08:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4c6c5ddc9fcf1628601e63e6226a35ce01359c83cfd9d1c015c4bb745e979`  
		Last Modified: Mon, 18 Aug 2025 23:08:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:5d151538c4529a61b5e38e137903d3184a9ac3bd6fe08b67ccda1f389ada0cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69907263d679a2c3acccfc36168c57c5d58cd27067848ce7c4336564f8be419`

```dockerfile
```

-	Layers:
	-	`sha256:d7400bccc5ebe6df4f853353ff842398d940a5fd19fb8af955d46ee8831f87b5`  
		Last Modified: Tue, 19 Aug 2025 00:20:11 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.4` - linux; s390x

```console
$ docker pull varnish@sha256:c51e07bde0f4bc684535b99752d6c1ffe5227d4da853252488991a929abbe8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87765648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb92f010b81bf7b2a702f526012301fb366911747300b8edb612188effe6c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70b7e13106db60c770a8a12e8bc1f58e629360de9920a64ca753f4c1317affb`  
		Last Modified: Mon, 18 Aug 2025 23:52:17 GMT  
		Size: 60.9 MB (60875764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82e7dd3d2496d842018db7d80b4ed31c6d31ff4d54a03acfdd56b6941dc8de7`  
		Last Modified: Mon, 18 Aug 2025 23:52:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85340c5d7e5955c218bb662463169bbed0cba4111fd0196e82e956f85cdf304`  
		Last Modified: Mon, 18 Aug 2025 23:52:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.4` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4dc9ddcbf370be0b20fc67f0af250e87a02e8a0da612fd59adb0718babbfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd44cc4240ede6fbf63a1cd21c22570ef6d60d3795dd5d14da4a9d3559184b0`

```dockerfile
```

-	Layers:
	-	`sha256:730f509db0663bf93c9fc9e1251a7a8e7921a33d088738d5dd20ac7969a869c6`  
		Last Modified: Tue, 19 Aug 2025 00:20:14 GMT  
		Size: 18.9 KB (18890 bytes)  
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

### `varnish:7.7` - linux; amd64

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; arm variant v7

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; arm64 variant v8

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; 386

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; ppc64le

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; s390x

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7.2` - linux; amd64

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

### `varnish:7.7.2` - unknown; unknown

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

### `varnish:7.7.2` - linux; arm variant v7

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

### `varnish:7.7.2` - unknown; unknown

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

### `varnish:7.7.2` - linux; arm64 variant v8

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

### `varnish:7.7.2` - unknown; unknown

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

### `varnish:7.7.2` - linux; 386

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

### `varnish:7.7.2` - unknown; unknown

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

### `varnish:7.7.2` - linux; ppc64le

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

### `varnish:7.7.2` - unknown; unknown

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

### `varnish:7.7.2` - linux; s390x

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

### `varnish:7.7.2` - unknown; unknown

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

### `varnish:fresh` - linux; amd64

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; arm variant v7

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; arm64 variant v8

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; 386

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; ppc64le

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; s390x

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

### `varnish:fresh` - unknown; unknown

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

## `varnish:old`

```console
$ docker pull varnish@sha256:22862d9143d6b1c489f434ce12640bfc4d7673d83423e221d28c3db291a313db
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
$ docker pull varnish@sha256:b092170cc8cb55549b1526dac8b8f64282f3e2669e58467c71c77ac73a58ff51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109946143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72ffe6810b784df3e44bddc8fec95bcaaf1425191ecb9b15623103105392442`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440cd84223df1ce32a4ecce96b18cd92436b79a32386a43d47021befaa35d9ca`  
		Last Modified: Mon, 18 Aug 2025 23:02:47 GMT  
		Size: 81.7 MB (81713848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe782b4816b6553b623cb27b82f2707908899ce8188699af63b33fd8e0c07c76`  
		Last Modified: Mon, 18 Aug 2025 23:02:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833de31c69510652b368756bc1516777d2fa5bb95467cd22b122645402d525e7`  
		Last Modified: Mon, 18 Aug 2025 23:02:43 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:c6933e8ef3c005edfad31453d9f6efb39183f962cfe08202e9d6717834628da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6341c78059c7be4fcae532f5a70ea56a5d3ce72ef20ed17f26c837a9f96f9086`

```dockerfile
```

-	Layers:
	-	`sha256:da89395ec937789492531a3f66e128f8a970f39adccfe3858f386eba3202aa35`  
		Last Modified: Tue, 19 Aug 2025 00:19:57 GMT  
		Size: 18.9 KB (18891 bytes)  
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
$ docker pull varnish@sha256:57b58ac36e1117b974c1608fee9aa420043c0015270538237cbde85fb66f79bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104466921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae84b77d8db5444cad5daf9297597a4c0f2bc89cb48af7b35d28655c81b8a0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66904f2fe198d1409d4d5b11a801d7c3c50b7addeb43a84322a068b404d2b`  
		Last Modified: Mon, 18 Aug 2025 23:04:56 GMT  
		Size: 76.4 MB (76382877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b87e4ebcc55ab78fbea549c0047e775d228e86a85afb389369517684db86c56`  
		Last Modified: Mon, 18 Aug 2025 23:04:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1062ff34d0d7890e63ea74a217ee3fb9f902a80beacf30f2f97a24d60bf22`  
		Last Modified: Mon, 18 Aug 2025 23:04:52 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e1e8507a8a81163188b75f69bed4371b82f2dc8063695958b2cc943de3a1af5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e2b7f8978ed026596049adaf1fdf7b354e68147e6d0f0dafd39b6ac55f4db9`

```dockerfile
```

-	Layers:
	-	`sha256:126f0f6aeabeb1bd9d4ba14911fb0a71d6a5a3fa2a88419f0e4623416031f326`  
		Last Modified: Tue, 19 Aug 2025 00:20:04 GMT  
		Size: 19.0 KB (18983 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:67358cd862134c4c44836bfbdcf3fd3d55a9d6b4f8e192ac32c00b06175f98d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107373844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d79c4681c14e1c40f6e6d18cc36222e2dfde5934bbe356817ef4ce8dd5ccd37`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
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
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068d73f957a05a45d0a78f12295db7e93429b1d5e0095b2b746eead4629087a7`  
		Last Modified: Mon, 18 Aug 2025 23:02:46 GMT  
		Size: 78.2 MB (78159195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ca2311c7318efd7145d539dc5fba5f51f53a6593f6e486d627dcb98027caaf`  
		Last Modified: Mon, 18 Aug 2025 23:02:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb795850fc867113d69da2ea60da2d2ebc851ba8e8729c591165badcb66d98e`  
		Last Modified: Mon, 18 Aug 2025 23:02:37 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:fcb941b07afd3706ba5bca42861cc60ad0a767125d0592c309421ae6e459155c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22807049c2bbc575a18540bc0c27532aecbe84b6b122939b22bca86dc82e8a25`

```dockerfile
```

-	Layers:
	-	`sha256:f9b83c3b60b750a0738872fe5d85e5c12833307403148fc1d0c4aa49e85ffce1`  
		Last Modified: Tue, 19 Aug 2025 00:20:07 GMT  
		Size: 18.9 KB (18864 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:ccdcb7601062d3e85a322afee0803947d1e7bb150240c7703791df7e9fea4558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c59d3a3e361556d3458fe10eb466ae200ec0ca685b864059468abe6fc656631`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5dcd21108357c0c849635f3aca97e0e649ab2867b7fa1874ef0e73a5ba1f09`  
		Last Modified: Mon, 18 Aug 2025 23:09:08 GMT  
		Size: 79.9 MB (79901047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b381c74c88b922841cdfcef3d27c5768858212296b6725b703ce68e95a6e819`  
		Last Modified: Mon, 18 Aug 2025 23:08:58 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4c6c5ddc9fcf1628601e63e6226a35ce01359c83cfd9d1c015c4bb745e979`  
		Last Modified: Mon, 18 Aug 2025 23:08:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5d151538c4529a61b5e38e137903d3184a9ac3bd6fe08b67ccda1f389ada0cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69907263d679a2c3acccfc36168c57c5d58cd27067848ce7c4336564f8be419`

```dockerfile
```

-	Layers:
	-	`sha256:d7400bccc5ebe6df4f853353ff842398d940a5fd19fb8af955d46ee8831f87b5`  
		Last Modified: Tue, 19 Aug 2025 00:20:11 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:c51e07bde0f4bc684535b99752d6c1ffe5227d4da853252488991a929abbe8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87765648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bb92f010b81bf7b2a702f526012301fb366911747300b8edb612188effe6c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70b7e13106db60c770a8a12e8bc1f58e629360de9920a64ca753f4c1317affb`  
		Last Modified: Mon, 18 Aug 2025 23:52:17 GMT  
		Size: 60.9 MB (60875764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82e7dd3d2496d842018db7d80b4ed31c6d31ff4d54a03acfdd56b6941dc8de7`  
		Last Modified: Mon, 18 Aug 2025 23:52:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85340c5d7e5955c218bb662463169bbed0cba4111fd0196e82e956f85cdf304`  
		Last Modified: Mon, 18 Aug 2025 23:52:09 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ae4dc9ddcbf370be0b20fc67f0af250e87a02e8a0da612fd59adb0718babbfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd44cc4240ede6fbf63a1cd21c22570ef6d60d3795dd5d14da4a9d3559184b0`

```dockerfile
```

-	Layers:
	-	`sha256:730f509db0663bf93c9fc9e1251a7a8e7921a33d088738d5dd20ac7969a869c6`  
		Last Modified: Tue, 19 Aug 2025 00:20:14 GMT  
		Size: 18.9 KB (18890 bytes)  
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
