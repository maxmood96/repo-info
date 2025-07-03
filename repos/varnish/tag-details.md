<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.14`](#varnish6014)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.3`](#varnish763)
-	[`varnish:7.6.3-alpine`](#varnish763-alpine)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.1`](#varnish771)
-	[`varnish:7.7.1-alpine`](#varnish771-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:3ea6c6c3c964ee4317d666960533c69ba5cfeae335191176e095d73c18617884
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
$ docker pull varnish@sha256:73855af0323500aec818851ac2775adb2075ba012849c6d9f7ae66a80a81871a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127755715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2416a3a733e0bcd8451f19dff388d0cf9639b7a4fb0405d453daf809ecf43c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a63fe15aa985166e0a536f16733c5108a400d7924f2d9e255c0fdc17483a7`  
		Last Modified: Tue, 01 Jul 2025 06:19:57 GMT  
		Size: 99.5 MB (99524819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f00144706708502c6ca62fad1808cc616a78de1f4fee6e717a406381d00957`  
		Last Modified: Tue, 01 Jul 2025 02:34:22 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:5fe26432899d928277277e73b7950a70acd3008bf3679cc61513798ad42d7d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93affad24d278f4006952a303dfaa72e03bf29ce2e335139a6661f6ed9ecf750`

```dockerfile
```

-	Layers:
	-	`sha256:d32a6c4b5e8d88ea5c052d0f6dbebca10055a0490091fe0dcf217eb5d131d823`  
		Last Modified: Tue, 01 Jul 2025 06:19:27 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d546048bdf9decdf83ff35b85c945c64424a2c45454947f90e642cfc3503c073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98278623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de534e855e7d7aff6838fdb59ef7d40f758aed1d6d6d9e1c9194a48aba036241`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e24917cd891f9d5ae1d2777c107e05262678dd8b4cbdd155454847751efae4`  
		Last Modified: Tue, 01 Jul 2025 08:57:10 GMT  
		Size: 74.3 MB (74339125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b947dec08812c0653ee92051ea8ac2e8a3e851428ec0b13da4ff64b47d3b86e`  
		Last Modified: Tue, 01 Jul 2025 08:57:01 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:17b3007883e565a862da70e5b58f360a7ccf12731ba26eb254091a966be4c966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8a889fd3b0a818870d5f6669753d69c950d72bced7b1b0ee53f592ac361bb1`

```dockerfile
```

-	Layers:
	-	`sha256:3e015e699a18830fefef9cdec2e6f3b8e74b9bc67f3e21b9919338e5fc8981f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:20 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:9669977c18b26fee22609b5c01222f19c027762ce8d7bdbd19c122f7e4cbc58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122404230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc62f49c5f4a4609748464d3a197cab21c8b8c2858a5e419a0ffed4b93720656`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52493f864a7ea7e76396f86bdf9e9c7e549171ff77a71cc23926691410bd561d`  
		Last Modified: Tue, 01 Jul 2025 15:19:43 GMT  
		Size: 94.3 MB (94325799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219e0aa2e5e7f385c96000801923cb3ec29cc5e47755b610005295fb6d077b1d`  
		Last Modified: Tue, 01 Jul 2025 12:14:45 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c244423326a51af935c87864c7662e4903d6f738ed0ff99503c4f985851314dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f3b8017bafae358fd913f470c57ae60a37452959455e7f92eb01f5cb281fa`

```dockerfile
```

-	Layers:
	-	`sha256:2e7bd3c8f173db3ad14d9576ca96736e9ca15c4a16d8e74df52832027cf6463c`  
		Last Modified: Tue, 01 Jul 2025 15:19:22 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:7a0cc82a8bf6f5bca7dd9d5b79271b3bead03d38e17de37a4d135885ca54e467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124893906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f392d5f8c15e9fcb5e91503f65e76a8f91ec8f76f1a430c6b0553c68c3d57d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28ce7101062bec3cdcc280044719a4889e578d9ea7e99a2c8cb2d0a7501eae3`  
		Last Modified: Tue, 01 Jul 2025 02:25:47 GMT  
		Size: 95.7 MB (95680721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1020eeb9c3c3d4471c4f899f48a869545850ee1e6547e0ddb6fe6214e8b4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c4d9adf6edc38a0e245fc98f12ccd3c0626821dd32664f93e4435d62e0d019d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd59d9b7ccc734ca895ead671fc640c07c4a91e57fb6c7610d30dcd61c3acdfe`

```dockerfile
```

-	Layers:
	-	`sha256:e278cb2e177cb76411294b2dca5e98bdf483723d9b1e47cba336321c581a45db`  
		Last Modified: Tue, 01 Jul 2025 06:19:38 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:12204804569c23f22cb919eeed20c6883c18abd2efa8b9e744600206fc2dd663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1a0f619b1a1cf8acac4b47a7c814d4b3b145b7bdc25d326ece1f645f32faa3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac448ec4ef6903243dd1113c4e835f8d6f94cf17ad1b7d098b60707fbe32ecff`  
		Last Modified: Tue, 01 Jul 2025 05:06:11 GMT  
		Size: 98.4 MB (98350777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24314fab222fef3f118c833876e2127208d2f66124d4d7ebb223e8ba890133c9`  
		Last Modified: Tue, 01 Jul 2025 05:06:05 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:13fe9ba79150b6df03dc2d839c7c31c96b9e6868cfeeef8a78b8cb06a86f0886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca147d055c4478a8c7e8aefd7063c243299125c951337eccc617a5ec76eb1b9a`

```dockerfile
```

-	Layers:
	-	`sha256:84730cad3bf1309e99d4cfcb85d846836681307eb9edd8b2f1258942d89d12bc`  
		Last Modified: Tue, 01 Jul 2025 06:19:41 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:9a4914672be907c1e84b32253dcb1534a3bc90ab9f91616acebd03858468e434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105638217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f4051bd3877ddaa96f1f5b121fbb0794e82fc712a0a92df06e42675e40766`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5e3acfd55d7be70f0cb0ec35643feeab794059804fb0394878dda0a1efc079`  
		Last Modified: Tue, 01 Jul 2025 05:30:02 GMT  
		Size: 78.7 MB (78749651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c1387deb44c299443963d18f577bc4de2ac7fefa0cff3a3f9a7db0b4caac8`  
		Last Modified: Tue, 01 Jul 2025 05:29:57 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f8370a2dc1663f730cc441d92918dd3e2b7fc3c18582a8e10b3e15aef66008ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c955f5c7a388140da8ecf7fd602133bfcd73fbe8a95337476358129b7adc9642`

```dockerfile
```

-	Layers:
	-	`sha256:4d0b37496975156f5b4be420ebe283b80fa298514487e5d05921f6fc7a6744a9`  
		Last Modified: Tue, 01 Jul 2025 06:19:44 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.14`

```console
$ docker pull varnish@sha256:3ea6c6c3c964ee4317d666960533c69ba5cfeae335191176e095d73c18617884
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

### `varnish:6.0.14` - linux; amd64

```console
$ docker pull varnish@sha256:73855af0323500aec818851ac2775adb2075ba012849c6d9f7ae66a80a81871a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127755715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2416a3a733e0bcd8451f19dff388d0cf9639b7a4fb0405d453daf809ecf43c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a63fe15aa985166e0a536f16733c5108a400d7924f2d9e255c0fdc17483a7`  
		Last Modified: Tue, 01 Jul 2025 06:19:57 GMT  
		Size: 99.5 MB (99524819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f00144706708502c6ca62fad1808cc616a78de1f4fee6e717a406381d00957`  
		Last Modified: Tue, 01 Jul 2025 02:34:22 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:5fe26432899d928277277e73b7950a70acd3008bf3679cc61513798ad42d7d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93affad24d278f4006952a303dfaa72e03bf29ce2e335139a6661f6ed9ecf750`

```dockerfile
```

-	Layers:
	-	`sha256:d32a6c4b5e8d88ea5c052d0f6dbebca10055a0490091fe0dcf217eb5d131d823`  
		Last Modified: Tue, 01 Jul 2025 06:19:27 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d546048bdf9decdf83ff35b85c945c64424a2c45454947f90e642cfc3503c073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98278623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de534e855e7d7aff6838fdb59ef7d40f758aed1d6d6d9e1c9194a48aba036241`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e24917cd891f9d5ae1d2777c107e05262678dd8b4cbdd155454847751efae4`  
		Last Modified: Tue, 01 Jul 2025 08:57:10 GMT  
		Size: 74.3 MB (74339125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b947dec08812c0653ee92051ea8ac2e8a3e851428ec0b13da4ff64b47d3b86e`  
		Last Modified: Tue, 01 Jul 2025 08:57:01 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:17b3007883e565a862da70e5b58f360a7ccf12731ba26eb254091a966be4c966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8a889fd3b0a818870d5f6669753d69c950d72bced7b1b0ee53f592ac361bb1`

```dockerfile
```

-	Layers:
	-	`sha256:3e015e699a18830fefef9cdec2e6f3b8e74b9bc67f3e21b9919338e5fc8981f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:20 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:9669977c18b26fee22609b5c01222f19c027762ce8d7bdbd19c122f7e4cbc58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122404230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc62f49c5f4a4609748464d3a197cab21c8b8c2858a5e419a0ffed4b93720656`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52493f864a7ea7e76396f86bdf9e9c7e549171ff77a71cc23926691410bd561d`  
		Last Modified: Tue, 01 Jul 2025 15:19:43 GMT  
		Size: 94.3 MB (94325799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219e0aa2e5e7f385c96000801923cb3ec29cc5e47755b610005295fb6d077b1d`  
		Last Modified: Tue, 01 Jul 2025 12:14:45 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:c244423326a51af935c87864c7662e4903d6f738ed0ff99503c4f985851314dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f3b8017bafae358fd913f470c57ae60a37452959455e7f92eb01f5cb281fa`

```dockerfile
```

-	Layers:
	-	`sha256:2e7bd3c8f173db3ad14d9576ca96736e9ca15c4a16d8e74df52832027cf6463c`  
		Last Modified: Tue, 01 Jul 2025 15:19:22 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; 386

```console
$ docker pull varnish@sha256:7a0cc82a8bf6f5bca7dd9d5b79271b3bead03d38e17de37a4d135885ca54e467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124893906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f392d5f8c15e9fcb5e91503f65e76a8f91ec8f76f1a430c6b0553c68c3d57d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28ce7101062bec3cdcc280044719a4889e578d9ea7e99a2c8cb2d0a7501eae3`  
		Last Modified: Tue, 01 Jul 2025 02:25:47 GMT  
		Size: 95.7 MB (95680721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1020eeb9c3c3d4471c4f899f48a869545850ee1e6547e0ddb6fe6214e8b4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:c4d9adf6edc38a0e245fc98f12ccd3c0626821dd32664f93e4435d62e0d019d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd59d9b7ccc734ca895ead671fc640c07c4a91e57fb6c7610d30dcd61c3acdfe`

```dockerfile
```

-	Layers:
	-	`sha256:e278cb2e177cb76411294b2dca5e98bdf483723d9b1e47cba336321c581a45db`  
		Last Modified: Tue, 01 Jul 2025 06:19:38 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; ppc64le

```console
$ docker pull varnish@sha256:12204804569c23f22cb919eeed20c6883c18abd2efa8b9e744600206fc2dd663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1a0f619b1a1cf8acac4b47a7c814d4b3b145b7bdc25d326ece1f645f32faa3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac448ec4ef6903243dd1113c4e835f8d6f94cf17ad1b7d098b60707fbe32ecff`  
		Last Modified: Tue, 01 Jul 2025 05:06:11 GMT  
		Size: 98.4 MB (98350777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24314fab222fef3f118c833876e2127208d2f66124d4d7ebb223e8ba890133c9`  
		Last Modified: Tue, 01 Jul 2025 05:06:05 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:13fe9ba79150b6df03dc2d839c7c31c96b9e6868cfeeef8a78b8cb06a86f0886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca147d055c4478a8c7e8aefd7063c243299125c951337eccc617a5ec76eb1b9a`

```dockerfile
```

-	Layers:
	-	`sha256:84730cad3bf1309e99d4cfcb85d846836681307eb9edd8b2f1258942d89d12bc`  
		Last Modified: Tue, 01 Jul 2025 06:19:41 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.14` - linux; s390x

```console
$ docker pull varnish@sha256:9a4914672be907c1e84b32253dcb1534a3bc90ab9f91616acebd03858468e434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105638217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f4051bd3877ddaa96f1f5b121fbb0794e82fc712a0a92df06e42675e40766`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5e3acfd55d7be70f0cb0ec35643feeab794059804fb0394878dda0a1efc079`  
		Last Modified: Tue, 01 Jul 2025 05:30:02 GMT  
		Size: 78.7 MB (78749651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c1387deb44c299443963d18f577bc4de2ac7fefa0cff3a3f9a7db0b4caac8`  
		Last Modified: Tue, 01 Jul 2025 05:29:57 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.14` - unknown; unknown

```console
$ docker pull varnish@sha256:f8370a2dc1663f730cc441d92918dd3e2b7fc3c18582a8e10b3e15aef66008ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c955f5c7a388140da8ecf7fd602133bfcd73fbe8a95337476358129b7adc9642`

```dockerfile
```

-	Layers:
	-	`sha256:4d0b37496975156f5b4be420ebe283b80fa298514487e5d05921f6fc7a6744a9`  
		Last Modified: Tue, 01 Jul 2025 06:19:44 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:9f57aef81284589ae063257f9d0244ceb1bb0879cd2fff32f8ec9aa0c2432988
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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4fefe8df5fecde1f9ecc6cc1c8fd8495d0e29a9e789d8e378507e2dd8f08281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104795466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645913d2da4cac3db624dceb37107a3a6732846f012e52193ae21702359eb0e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9260a9093c169ff66cf07680f7ad29921302f6f7c787dbb6f11d2b5408e967a`  
		Last Modified: Tue, 01 Jul 2025 08:51:13 GMT  
		Size: 80.9 MB (80854679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f5e3e112086012e875c48625845ddcda86fda4b350488076bf70f2c0fb1db`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d2856fcfca49973626913facafc24d441c7d798e5bf45f8ade15a77fc5d3d`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:3014215753f651a12948038fcd94caa0e267fdc2d8c6127ea6811e9f4e5e8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8f3144bc7874e6dbcdadbab7304d4df71a31c3d5c7199b37203e37251692d`

```dockerfile
```

-	Layers:
	-	`sha256:7cee7041929ae490f77027772083670dd4e0d5b1b963788897ef9dea2d8b57f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:30 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b8ce72f9171467b5087f915e4724d198758a50f3600251f84ddc40415c2e6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128782240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28b0bd963eec8028fbcfd095410239bc81899873d9ac3993b8b00a4c005ee1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a36cfc1a32abdd38315b21dc7d982dc81502c01c3d731fcad2f110f057f37f`  
		Last Modified: Tue, 01 Jul 2025 06:49:21 GMT  
		Size: 100.7 MB (100702515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3386165ac1e78d913cca676585f17b3d3085d8d106771b0c95257dd19b211438`  
		Last Modified: Tue, 01 Jul 2025 06:48:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2b8fa324fd60ea700c3952a12505fe90202e805ea1acd941cb02a63766ca2`  
		Last Modified: Tue, 01 Jul 2025 06:48:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:2707221f195aa28c3f78132f6cc9c0fc292d52eb38cbb035988a91f49223823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cf22dae8faf4485734811bbe5474e1ab14bbb3430b3767f6d163715653049`

```dockerfile
```

-	Layers:
	-	`sha256:d940665171e4f9ebacd8803d861f792ef657925a7431742bb54ba647f2950894`  
		Last Modified: Tue, 01 Jul 2025 09:19:33 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; ppc64le

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

### `varnish:7` - unknown; unknown

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

### `varnish:7` - linux; s390x

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

### `varnish:7` - unknown; unknown

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

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:cc0a7aad884e7e86b751fbb031c56ebee7bef90fe3b05b3272aa58322bfe0af6
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
$ docker pull varnish@sha256:e68dc9857076551f8a67225317a95f345ad91e1f11c46c34210a7291adca6967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80315725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9095c515e21eb54100068f9a2ecfb3955655c2ee88fef95f72e3ccb6db24e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37e905a5b0a7e3887b2a91c8327b24129284a0d4f3951d3d9c1bc2c311a62d`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 76.7 MB (76671419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deacc4f5ce53935aa92bcf316166edecb88d737a471b0c6ca0bf48473cc100e`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d05040e8ab5a7400a08463a05466ce025243a468968194a57f9d867ed71c4`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:073fbd63633e8cfd353e4ec52c591ba2ac33e0e754cfb31912e3e78c8c0e2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23415dee6df89120996803f92b9564456f2f811d2762c918a334bafcdec5278`

```dockerfile
```

-	Layers:
	-	`sha256:018e7686fef92c81e6d79fd1f1bd13969950d4398f0435fad294561c8af9547a`  
		Last Modified: Wed, 04 Jun 2025 22:50:23 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:00ac6b75c1690c74500ec45b30a46a8760a81a908c866bff46a826f6d6d46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62366095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240af100b3925d63c86bcc69ff57620fcbc327ba2ba5ace25bb0e38926a2fdd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277c43e2a6e7ca8224b892d8251fd2f8944eb81fd376d90c5240f7816a0f083`  
		Last Modified: Thu, 03 Jul 2025 03:49:30 GMT  
		Size: 59.3 MB (59265914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd3f2d2fac3ed373219e2f04eb8c553a4b9cd07f49822a348cd6bd0ba0bf03`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107ef22442871d82b7ec5388ec01e3e2959a9e0e457bb531af8f317f1835928`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7350079942c472339e1816bfd7c6aedd38cc60d56c537313b4dd72db0413bc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a141db0e280fa2f137f3bd523ff5c2742c2efe54f70ea8fc5b7b2ed71f6168`

```dockerfile
```

-	Layers:
	-	`sha256:ca90931822ce458bc12a86e23a88bd82f7c8417c72e440a288c63ba1980187de`  
		Last Modified: Thu, 03 Jul 2025 03:50:35 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0f90786ecfa0f4e952a8bfcd7cf90ffb65f55afe12a1038b44d230554da349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77317664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a8e20c8b0476e94c93500537b71b2d6c9be6fbf759d39ebf428c5825cdf764`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84cd3f100e7a4987c9955b88d2ef87afc93a0e64cd6d8aa10263812165fe27`  
		Last Modified: Tue, 03 Jun 2025 14:12:57 GMT  
		Size: 73.3 MB (73322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f9e26ec65432a8efe09f77a816bf77b643748294604f7eeedb1601897d54`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204ee6311ecdf7dd9255ffe86d6389a3da94408d715faa19f1d7c770750e654`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1fc387008de696d9c88f44df0d8657685c27996c772c00f3d72fbf60635b7557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c364243c247b5f5a8019e10d2800233ed9c74c18cda92e040fcae27072732a`

```dockerfile
```

-	Layers:
	-	`sha256:9886a9295fbfcfb2c559ef20677457a21cea3b439be5bb62329e04ff2d942936`  
		Last Modified: Thu, 03 Jul 2025 03:51:56 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b121f54ac7f5b5c56b4247fd3a89f5eaa87edb49536a78080a31283009af079c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82508852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09ad2b11367485e00ad4bfd5a72c959b265f7da89c593cb821cd1bd3a31f35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c61829aa639dff24aad65e1a82bc8d02bf867875e2d4c5e53137c5276cb2d1`  
		Last Modified: Thu, 03 Jul 2025 03:52:07 GMT  
		Size: 79.0 MB (79043172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960eea97cf4f85503b6f86d972a55d352d8befc1bb5ce313e3afd030bde0419`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f18cbf086639292a7cf6ea4ef41ea5008005b3aaad98bac0c1e90b1d31838a`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d1466d9b377d819bd92e5f57939cb0c6d678cbfeda41f7364e267c23ad3635d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75d8d35091397ece88fcbfedf8015f162f250dfa08ba6c4d34d51e129502f7`

```dockerfile
```

-	Layers:
	-	`sha256:1acecb9b3a5cda019c5227afed2ea18570ffeaeb102971e5262e9ae248497b27`  
		Last Modified: Thu, 03 Jul 2025 03:53:16 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:71d583672fd210f53a87283c6cd7d8f0724cb438133803dcc2efddc983a4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76438752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9699c43a7e79fb04a4be6186b24690ad97f4e62825ee80eff8b1c7d7e0f210`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbab925e54587cbf4497c7970617c093c097ad8c8130f3f3683fca36278df31`  
		Last Modified: Thu, 03 Jul 2025 03:53:27 GMT  
		Size: 72.9 MB (72862344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb5bd15cbeac020aacb495032517a81a030115e97271921f08eb49865f0045`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b52ba2323f2f33051b67003e5f5ccb783f00ff3b7aa934e8d32dbea2c1860`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d94a917abc20ae0e4c8bc4e8f7f1d2945a698b16383f1f33a790aad4876148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c61ed2fadd3eb862006a0a17f29ccc99948148d5f87e0a3ee70403c5c3616c`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a360fb74bcf4bac9f6756708403acf376b869d1fb1bab0b248394b4b0fcfb`  
		Last Modified: Thu, 03 Jul 2025 03:54:30 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d11e359e354542668965c74d14c43927f83784083bff1786e638ab48d378112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73df919373dc10e0f84e083bf120e846c130d92fffa1442e1f8bc4441b7a7c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b83f7ad8b83b5dcd56c2bd88b05dac6dbb70832ec12eecc3357cf097f7557`  
		Last Modified: Thu, 03 Jul 2025 03:54:40 GMT  
		Size: 67.6 MB (67564885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacd333e5c4954b9a8d9f90265c801e8336cd7c6961afdc4b95da8145104dec`  
		Last Modified: Thu, 03 Jul 2025 03:55:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2611d5ee154f2c95fdcb474c498be2f8f0689c6c70cc4fa28acb770361e34fc`  
		Last Modified: Thu, 03 Jul 2025 03:55:40 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f1c5fa2662bf90956b5c270950cf6d6f2f8a1e3cf0aef9716aaa47400cc6afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188aab5b4924a51bfbd764a58d62bd7339a56f5b27faa5f8079ca6b60cf58257`

```dockerfile
```

-	Layers:
	-	`sha256:705f3871102b5aba5628f7eabccfed1d5bc984c5e7197744e5d5633ae2f279d5`  
		Last Modified: Thu, 03 Jul 2025 03:55:44 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:f29b8e672ee825ce9e1c140af30692d2861785d45598709a7fdabe14736fb847
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
$ docker pull varnish@sha256:a07aff90a2582813f488b78a2cfa19e94533b92795fb2a8244a88875316774cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134236559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc048330b90e42aaddb7790bfa04d84fe03c492eca052304a25accff377353b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0891dd165e99b1eeb33af028ca85c451665cab5dfad0dc64f62b095d3b3aaf6e`  
		Last Modified: Tue, 01 Jul 2025 02:27:47 GMT  
		Size: 106.0 MB (106004377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c7ea422e8b12db1fbbc1cf1a306e02b5920b4838b917ccee0ed8d084e6fd9e`  
		Last Modified: Tue, 01 Jul 2025 02:27:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61655fca1b3e119f885d50ef25e5aebf9983ca4e15a6948c60c71d869830d51e`  
		Last Modified: Tue, 01 Jul 2025 02:27:32 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:6111454f49c12594f4f561fd3cb8d7e276c8f627d29ed03c5b002f5c5bfae6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af92e5ec85c0a42ea6fb924b8d704003a5c3ce62b4c3dfeea90e6e5772301940`

```dockerfile
```

-	Layers:
	-	`sha256:b728358d599001cb63131dd0187e0f00e591734d0a0585599900399e9870db0b`  
		Last Modified: Tue, 01 Jul 2025 06:19:54 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:da73f1c62c251a64681e9b0fc6bbfecfb6deb90cb3a047fe13b4442954055e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104595629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568675fe6f88f6af128d414ac2f5696675d4d75c148439bd2720000a8d98a65c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6458e3abbb227c914e1a49bee2e4f51c15ae4b98536784a041989965ac9ba1`  
		Last Modified: Tue, 01 Jul 2025 08:54:37 GMT  
		Size: 80.7 MB (80654837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024765d4f507e1d448078f2ff108b09cb0cef092c51642ae9211ce0a287ee29f`  
		Last Modified: Tue, 01 Jul 2025 08:54:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923df3354dd245a18916c4c74165caacd4c7de9994df44a6f9c29c8c66dd5f30`  
		Last Modified: Tue, 01 Jul 2025 08:54:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:abf0bb1c6aa0f2a0aeaa02a82a66856b2ae7b9815460c7132705d4d64989189c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e55b80eeee1f9fc1312c99d8c706e7dc642da4ad77c9b11818b9d8d412964`

```dockerfile
```

-	Layers:
	-	`sha256:59217e4edfc13af6b706ecacce82c23f7f84311c21c96fbf965dbb4e5e5c979e`  
		Last Modified: Tue, 01 Jul 2025 09:19:39 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2c9176807cb717e08edeaedf06863fe899b2d3d467a68eac824ae3e8843115a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128572969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef59fc06dbb57e6c0774103450f2ddf98ad6cc77f2d531df9070c294828573f9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e83a9c02989fa1f23897fd29799a0b7b2d3bff0e00ee8695c282d8bce3a242`  
		Last Modified: Tue, 01 Jul 2025 06:51:28 GMT  
		Size: 100.5 MB (100493245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16c098d7835542322bf64895feb17747c337fbd88c5485ca6fb78efe05ccf2`  
		Last Modified: Tue, 01 Jul 2025 06:51:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66b57aa3ca84bf7af5702d3cf511afb9699705e894837f7c14452ff16a587f6`  
		Last Modified: Tue, 01 Jul 2025 06:51:23 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:989bc63306ee66c9685a7d48d4142f1cf737b828277fdba121e829ec61d0f7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d00b20f9917fb609d9bc6fe50c727abb839ee7850e3aeb63832d7eb7033047`

```dockerfile
```

-	Layers:
	-	`sha256:97406f57931533547a7e3e141bfcd9ec9a7ae289e06bc677ca7a8a68a75475db`  
		Last Modified: Tue, 01 Jul 2025 09:19:42 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:84847ab9ccd5263018f014b382c13955fe1cc0c9b1a86d681971bdfba0de396a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131369924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24026a222474b539b5fc5edd99e115bf9523b5200b7a61f360c5db336052a42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc201735ad38a34f7d5941fc5f8e6e60bc0d0788c3ccbe7410436d553aea07`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 102.2 MB (102155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691102731be20916f7fe89899c11fc5ba76a2125f540757cc1be3c7c75caa183`  
		Last Modified: Tue, 01 Jul 2025 02:27:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f19e2f6820f0f2da871a873a709d4c67a4896adda3aca3cb98e1fa60687712`  
		Last Modified: Tue, 01 Jul 2025 02:27:18 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:7b6f92667483bfbd6210215a2587d693e6bce569b9ddb727cedc06fcee253a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5622681e44babbab58efeb45865ee0d5f5b0d125071a8d0f0239c423d107e9`

```dockerfile
```

-	Layers:
	-	`sha256:fd7721d58c7f4bf5b7192725c7a087aa85ad66aaf0c7354caeb41709c5adfda0`  
		Last Modified: Tue, 01 Jul 2025 06:20:05 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:02a913b6eacdf1f73d365966758b470e9c83d82bbc29d051f3c744018494bf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137051120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec4009d395c697dd2483d65780aca3c111425d0d442bdd5cd97f59d87db5fda`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96efbee2c552a9cf474e05a34f3262b0646bdf50fb24c73dc5492ebfe7c6f55f`  
		Last Modified: Tue, 01 Jul 2025 05:02:18 GMT  
		Size: 105.0 MB (104976253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7897143b748b83eb00fb95941d339eee8ff4dca883cdcb08c15fd0dadf9b3c`  
		Last Modified: Tue, 01 Jul 2025 05:02:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865829d57248d93931e9aeb809eaef2a3de0f94c66def6fb0bcfec1431b18991`  
		Last Modified: Tue, 01 Jul 2025 05:02:12 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:0dae0834473849a40c76a068d13890ace8f971d4cbde19d19b3fdee2ffe24e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81dadbef890e2d2483a97d716f001299537d461cdc7b355705b5ec2e90aa491`

```dockerfile
```

-	Layers:
	-	`sha256:a096e433f15d58b286f6f1cd45384cf1307798a8058cf30228a5fafe1e7ffd96`  
		Last Modified: Tue, 01 Jul 2025 06:20:08 GMT  
		Size: 18.9 KB (18885 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:d75dfa792b2c3979f84f6a00ae9c604ce8cdd63c49035cccde96fec2d396a73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112154499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b762437511e13ce33d1ce9e0d1fec726e3deda2822a4810a86c1017858bd739`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df2af803aa4e058f2551625308c7bb768a5a05ca93d14c6b813a07614ea8e0`  
		Last Modified: Tue, 01 Jul 2025 05:30:00 GMT  
		Size: 85.3 MB (85264642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdb789262a66091a769d34bc03648f88a07516966a157555ba43792771d9ba2`  
		Last Modified: Tue, 01 Jul 2025 05:29:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c269b94e20d7e9081e9bfb22d164a943cbdeeae12bc3971d32837b846590b1f7`  
		Last Modified: Tue, 01 Jul 2025 05:29:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:1cef0831a5e455416dadba79fef6302d40425187a7cc10a78f9cd82bcd3023e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b27bdee97d78442609432a7107ec22559cab4b6b79220ce79c5e831b9d90c4`

```dockerfile
```

-	Layers:
	-	`sha256:5f37e177e2913803da34c7c1a57ce635021502dac0f2471ecde5927420dce122`  
		Last Modified: Tue, 01 Jul 2025 06:20:12 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:cb268b57c8a2cec3d39e8e4f74382646c8795718ff25aa57c0d0a5ee3eb1146f
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
$ docker pull varnish@sha256:832539f3c49155c868d6e605b23d11635697ee79308d4d67632bfd80a3592470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef6a698cd1a97012baa9bdd2db973a223ae7b7500b68afd5d7a2849cffaf42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd875d896754e31f106b279b13f6496adc8421db2c4f87731e3e4723097d55`  
		Last Modified: Fri, 16 May 2025 13:21:30 GMT  
		Size: 76.5 MB (76480503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e6d4496a56a4cdc28e0728f444aca412abcdbf44de2a17517f260143d2445`  
		Last Modified: Thu, 15 May 2025 20:16:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2dce4d3db4cb8f19e79b85dd340da315f5a6503c0177d857e7d710bad2e19`  
		Last Modified: Thu, 15 May 2025 20:24:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:745b542be3ade7260c951fd0df6eb7803b1d483c633be4bbe214419631ee5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc11303947e59091cf3071eab27aa971a25b9b73cfbb7832b60329497a50ab`

```dockerfile
```

-	Layers:
	-	`sha256:f89f56e4fa97bf3b52dbeb162f579e87f78751ccf4665eafdf273436ff4d5639`  
		Last Modified: Wed, 04 Jun 2025 22:49:56 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c6f15a90cf4d116fb28f39ecb012995aefb0ecd49c02fa0bd9aeec4adf65cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348b5a86113885af2ad1ae03b67a656675d858bac28550d8756c22fb352073a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b64d240de8405e58901ffaa351cf6d995f373610fee29e4806ebafbe8f51b4`  
		Last Modified: Tue, 13 May 2025 23:54:33 GMT  
		Size: 59.1 MB (59076980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f345bef6ca24ad7825007178523af189952fa489de9d8eb18ddad503404c52e`  
		Last Modified: Thu, 15 May 2025 20:17:20 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb03c9836d2f802ac7a200af8b7b5a3d37f070eb40a1fca06426d08cf583d3`  
		Last Modified: Thu, 15 May 2025 20:27:18 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:341536aa96b8653cdc7655ab75a700a74a413abb92fbd62c9736a51d288996b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ccd8901dac22a6fcb8114bc93626ea4a138d3c97c173fc51ce70e0fff5f590`

```dockerfile
```

-	Layers:
	-	`sha256:9df71e7bf646620391b06844710aa5d6a127203721dbbdce0a0b070fe4301319`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:03050dcb8e1b8c436dd6bb97d15cd02ce355fb92d5b0f4fd2a9d87236bacd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12c01235c01884aba1beb3ce7e3764811403422085d6361e69b7f7e89a142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d0112c73e93ba409991084c46b91c454e8873ad85d1a0c704da073c738110`  
		Last Modified: Fri, 16 May 2025 20:41:39 GMT  
		Size: 73.1 MB (73139804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5db8d46da3afc53cd359504e09f6a3822ceefd1859d19b3d76bcffdefa2e7`  
		Last Modified: Thu, 15 May 2025 20:29:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afac65ae6f31067843e3de68aa1266f07ddce142c1ae08692d23030bee350b`  
		Last Modified: Thu, 15 May 2025 20:23:07 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:79357498a90f86e478600efa6dccae02abc17f66981aec1940ea28ced6fd52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d5e0e50d45a1f2ae76d217647b08bca1f59442495bc5c01e2f0ba8c9079ca`

```dockerfile
```

-	Layers:
	-	`sha256:56e88217b045f05b58b9caa245c23fded45cf4a2be1d1c230f34b1b574fb44e4`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:501e68fff243f1b20a14eb50b92274eb17d3668b18614971adbe63c11f567f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82330387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee568acabd5eb2489c8492d7ccfa16f09434e29b4969f6f9772f2e41aa022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b78442a5d78ba9003dcc9cdc85c9df4f9cfafb1ad42b203d6ac1ea49040aab4`  
		Last Modified: Tue, 13 May 2025 23:48:04 GMT  
		Size: 78.9 MB (78864705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b116832fccbcf9a985576f61c96fe8c6bd152de5d63b1d3584e815df6cc8030`  
		Last Modified: Thu, 15 May 2025 20:15:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004edc5aa7acec0262bd1823f0da31ecb8e70efaf37858b2ea6ca28bf441780e`  
		Last Modified: Thu, 15 May 2025 20:21:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09e44671e22716a149f4d002f38e34628f91c212ba0e3057686c99a07ab0e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286f1515be59ef428b8da884b540ac598ed7f2a8b8e6f64ea9635f564882715`

```dockerfile
```

-	Layers:
	-	`sha256:725f13bcaad1fad6dc735aa5a28fbbe6d5b682b7282865560844161fc6878b0b`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f71a73be8317c4072b991ee98c4c3d8eadb24d188800178968beb834c5724d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76254322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39867711695ca6650e67c074879731c99cebcdfc99080d153b82a437bbd0c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9b258186a0fcc1c5c8c94beeb1d5bb81c0ab46f616ce67e7a00bf431cc4a3`  
		Last Modified: Wed, 14 May 2025 00:00:26 GMT  
		Size: 72.7 MB (72677915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e89d21db4cd9964b28450f72cf636a52889cfe69f1d4cb2f242a5a3d2ad350`  
		Last Modified: Thu, 15 May 2025 20:15:42 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b02ea0fef7a75f4975001831e3cc80c4fc8904726393c3c240acce25932a96`  
		Last Modified: Thu, 15 May 2025 20:20:52 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b8bb1c1c7e7e8608aacbef7f0b606beb2db199da80c18d189ad22ba69cf00370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6951c078ba75ba3eb2418cecd3a1e5b91a4373905eabd1a4d5caee74b8d56e9`

```dockerfile
```

-	Layers:
	-	`sha256:cfc6a58d241c77836c04f39e0e1a7adfe81d3ee28a3f7889eec06d865211a268`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:01893f1c5743b8d2b36383618902945cba7b093649f09519ebe158ba9f5f8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70859326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd196cc640f60dfe5eaa365485db2e8c6aac01a37f71995a8895ac495f0e5587`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58c2794411aa50dc12dbb79cdf53b10c92442248361dbe2644b83e7d4d2ba`  
		Last Modified: Tue, 13 May 2025 23:56:19 GMT  
		Size: 67.4 MB (67389700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824335bb1eb8cfc81d98eb1052441a94a5806fa9e3d060cb71f520520d0bf74`  
		Last Modified: Thu, 15 May 2025 20:22:31 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31dbfe4dde5d97940cea5e1c9a3d64dbc3d17c8aaba5d04926e5a54fe250069`  
		Last Modified: Thu, 15 May 2025 20:26:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82c172006540f09f9dd5322d8d9f23fda47f1ad037a7196f60115a40f504927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75b90bd5fa7d9fccf356e10d78df6ec4e00a7a88ad8dd24d0ec915d5e64412`

```dockerfile
```

-	Layers:
	-	`sha256:68c68e03488141b66b6f577ded0927247796d3cc30661286e556cf227077b16c`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.3`

```console
$ docker pull varnish@sha256:f29b8e672ee825ce9e1c140af30692d2861785d45598709a7fdabe14736fb847
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

### `varnish:7.6.3` - linux; amd64

```console
$ docker pull varnish@sha256:a07aff90a2582813f488b78a2cfa19e94533b92795fb2a8244a88875316774cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134236559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc048330b90e42aaddb7790bfa04d84fe03c492eca052304a25accff377353b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0891dd165e99b1eeb33af028ca85c451665cab5dfad0dc64f62b095d3b3aaf6e`  
		Last Modified: Tue, 01 Jul 2025 02:27:47 GMT  
		Size: 106.0 MB (106004377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c7ea422e8b12db1fbbc1cf1a306e02b5920b4838b917ccee0ed8d084e6fd9e`  
		Last Modified: Tue, 01 Jul 2025 02:27:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61655fca1b3e119f885d50ef25e5aebf9983ca4e15a6948c60c71d869830d51e`  
		Last Modified: Tue, 01 Jul 2025 02:27:32 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:6111454f49c12594f4f561fd3cb8d7e276c8f627d29ed03c5b002f5c5bfae6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af92e5ec85c0a42ea6fb924b8d704003a5c3ce62b4c3dfeea90e6e5772301940`

```dockerfile
```

-	Layers:
	-	`sha256:b728358d599001cb63131dd0187e0f00e591734d0a0585599900399e9870db0b`  
		Last Modified: Tue, 01 Jul 2025 06:19:54 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:da73f1c62c251a64681e9b0fc6bbfecfb6deb90cb3a047fe13b4442954055e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104595629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568675fe6f88f6af128d414ac2f5696675d4d75c148439bd2720000a8d98a65c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6458e3abbb227c914e1a49bee2e4f51c15ae4b98536784a041989965ac9ba1`  
		Last Modified: Tue, 01 Jul 2025 08:54:37 GMT  
		Size: 80.7 MB (80654837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024765d4f507e1d448078f2ff108b09cb0cef092c51642ae9211ce0a287ee29f`  
		Last Modified: Tue, 01 Jul 2025 08:54:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923df3354dd245a18916c4c74165caacd4c7de9994df44a6f9c29c8c66dd5f30`  
		Last Modified: Tue, 01 Jul 2025 08:54:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:abf0bb1c6aa0f2a0aeaa02a82a66856b2ae7b9815460c7132705d4d64989189c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e55b80eeee1f9fc1312c99d8c706e7dc642da4ad77c9b11818b9d8d412964`

```dockerfile
```

-	Layers:
	-	`sha256:59217e4edfc13af6b706ecacce82c23f7f84311c21c96fbf965dbb4e5e5c979e`  
		Last Modified: Tue, 01 Jul 2025 09:19:39 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2c9176807cb717e08edeaedf06863fe899b2d3d467a68eac824ae3e8843115a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128572969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef59fc06dbb57e6c0774103450f2ddf98ad6cc77f2d531df9070c294828573f9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e83a9c02989fa1f23897fd29799a0b7b2d3bff0e00ee8695c282d8bce3a242`  
		Last Modified: Tue, 01 Jul 2025 06:51:28 GMT  
		Size: 100.5 MB (100493245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16c098d7835542322bf64895feb17747c337fbd88c5485ca6fb78efe05ccf2`  
		Last Modified: Tue, 01 Jul 2025 06:51:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66b57aa3ca84bf7af5702d3cf511afb9699705e894837f7c14452ff16a587f6`  
		Last Modified: Tue, 01 Jul 2025 06:51:23 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:989bc63306ee66c9685a7d48d4142f1cf737b828277fdba121e829ec61d0f7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d00b20f9917fb609d9bc6fe50c727abb839ee7850e3aeb63832d7eb7033047`

```dockerfile
```

-	Layers:
	-	`sha256:97406f57931533547a7e3e141bfcd9ec9a7ae289e06bc677ca7a8a68a75475db`  
		Last Modified: Tue, 01 Jul 2025 09:19:42 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; 386

```console
$ docker pull varnish@sha256:84847ab9ccd5263018f014b382c13955fe1cc0c9b1a86d681971bdfba0de396a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131369924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24026a222474b539b5fc5edd99e115bf9523b5200b7a61f360c5db336052a42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc201735ad38a34f7d5941fc5f8e6e60bc0d0788c3ccbe7410436d553aea07`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 102.2 MB (102155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691102731be20916f7fe89899c11fc5ba76a2125f540757cc1be3c7c75caa183`  
		Last Modified: Tue, 01 Jul 2025 02:27:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f19e2f6820f0f2da871a873a709d4c67a4896adda3aca3cb98e1fa60687712`  
		Last Modified: Tue, 01 Jul 2025 02:27:18 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:7b6f92667483bfbd6210215a2587d693e6bce569b9ddb727cedc06fcee253a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5622681e44babbab58efeb45865ee0d5f5b0d125071a8d0f0239c423d107e9`

```dockerfile
```

-	Layers:
	-	`sha256:fd7721d58c7f4bf5b7192725c7a087aa85ad66aaf0c7354caeb41709c5adfda0`  
		Last Modified: Tue, 01 Jul 2025 06:20:05 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:02a913b6eacdf1f73d365966758b470e9c83d82bbc29d051f3c744018494bf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137051120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec4009d395c697dd2483d65780aca3c111425d0d442bdd5cd97f59d87db5fda`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96efbee2c552a9cf474e05a34f3262b0646bdf50fb24c73dc5492ebfe7c6f55f`  
		Last Modified: Tue, 01 Jul 2025 05:02:18 GMT  
		Size: 105.0 MB (104976253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7897143b748b83eb00fb95941d339eee8ff4dca883cdcb08c15fd0dadf9b3c`  
		Last Modified: Tue, 01 Jul 2025 05:02:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865829d57248d93931e9aeb809eaef2a3de0f94c66def6fb0bcfec1431b18991`  
		Last Modified: Tue, 01 Jul 2025 05:02:12 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:0dae0834473849a40c76a068d13890ace8f971d4cbde19d19b3fdee2ffe24e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81dadbef890e2d2483a97d716f001299537d461cdc7b355705b5ec2e90aa491`

```dockerfile
```

-	Layers:
	-	`sha256:a096e433f15d58b286f6f1cd45384cf1307798a8058cf30228a5fafe1e7ffd96`  
		Last Modified: Tue, 01 Jul 2025 06:20:08 GMT  
		Size: 18.9 KB (18885 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3` - linux; s390x

```console
$ docker pull varnish@sha256:d75dfa792b2c3979f84f6a00ae9c604ce8cdd63c49035cccde96fec2d396a73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112154499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b762437511e13ce33d1ce9e0d1fec726e3deda2822a4810a86c1017858bd739`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df2af803aa4e058f2551625308c7bb768a5a05ca93d14c6b813a07614ea8e0`  
		Last Modified: Tue, 01 Jul 2025 05:30:00 GMT  
		Size: 85.3 MB (85264642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdb789262a66091a769d34bc03648f88a07516966a157555ba43792771d9ba2`  
		Last Modified: Tue, 01 Jul 2025 05:29:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c269b94e20d7e9081e9bfb22d164a943cbdeeae12bc3971d32837b846590b1f7`  
		Last Modified: Tue, 01 Jul 2025 05:29:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3` - unknown; unknown

```console
$ docker pull varnish@sha256:1cef0831a5e455416dadba79fef6302d40425187a7cc10a78f9cd82bcd3023e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b27bdee97d78442609432a7107ec22559cab4b6b79220ce79c5e831b9d90c4`

```dockerfile
```

-	Layers:
	-	`sha256:5f37e177e2913803da34c7c1a57ce635021502dac0f2471ecde5927420dce122`  
		Last Modified: Tue, 01 Jul 2025 06:20:12 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.3-alpine`

```console
$ docker pull varnish@sha256:cb268b57c8a2cec3d39e8e4f74382646c8795718ff25aa57c0d0a5ee3eb1146f
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

### `varnish:7.6.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:832539f3c49155c868d6e605b23d11635697ee79308d4d67632bfd80a3592470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef6a698cd1a97012baa9bdd2db973a223ae7b7500b68afd5d7a2849cffaf42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd875d896754e31f106b279b13f6496adc8421db2c4f87731e3e4723097d55`  
		Last Modified: Fri, 16 May 2025 13:21:30 GMT  
		Size: 76.5 MB (76480503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e6d4496a56a4cdc28e0728f444aca412abcdbf44de2a17517f260143d2445`  
		Last Modified: Thu, 15 May 2025 20:16:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2dce4d3db4cb8f19e79b85dd340da315f5a6503c0177d857e7d710bad2e19`  
		Last Modified: Thu, 15 May 2025 20:24:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:745b542be3ade7260c951fd0df6eb7803b1d483c633be4bbe214419631ee5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc11303947e59091cf3071eab27aa971a25b9b73cfbb7832b60329497a50ab`

```dockerfile
```

-	Layers:
	-	`sha256:f89f56e4fa97bf3b52dbeb162f579e87f78751ccf4665eafdf273436ff4d5639`  
		Last Modified: Wed, 04 Jun 2025 22:49:56 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c6f15a90cf4d116fb28f39ecb012995aefb0ecd49c02fa0bd9aeec4adf65cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348b5a86113885af2ad1ae03b67a656675d858bac28550d8756c22fb352073a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b64d240de8405e58901ffaa351cf6d995f373610fee29e4806ebafbe8f51b4`  
		Last Modified: Tue, 13 May 2025 23:54:33 GMT  
		Size: 59.1 MB (59076980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f345bef6ca24ad7825007178523af189952fa489de9d8eb18ddad503404c52e`  
		Last Modified: Thu, 15 May 2025 20:17:20 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb03c9836d2f802ac7a200af8b7b5a3d37f070eb40a1fca06426d08cf583d3`  
		Last Modified: Thu, 15 May 2025 20:27:18 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:341536aa96b8653cdc7655ab75a700a74a413abb92fbd62c9736a51d288996b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ccd8901dac22a6fcb8114bc93626ea4a138d3c97c173fc51ce70e0fff5f590`

```dockerfile
```

-	Layers:
	-	`sha256:9df71e7bf646620391b06844710aa5d6a127203721dbbdce0a0b070fe4301319`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:03050dcb8e1b8c436dd6bb97d15cd02ce355fb92d5b0f4fd2a9d87236bacd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12c01235c01884aba1beb3ce7e3764811403422085d6361e69b7f7e89a142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d0112c73e93ba409991084c46b91c454e8873ad85d1a0c704da073c738110`  
		Last Modified: Fri, 16 May 2025 20:41:39 GMT  
		Size: 73.1 MB (73139804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5db8d46da3afc53cd359504e09f6a3822ceefd1859d19b3d76bcffdefa2e7`  
		Last Modified: Thu, 15 May 2025 20:29:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afac65ae6f31067843e3de68aa1266f07ddce142c1ae08692d23030bee350b`  
		Last Modified: Thu, 15 May 2025 20:23:07 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:79357498a90f86e478600efa6dccae02abc17f66981aec1940ea28ced6fd52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d5e0e50d45a1f2ae76d217647b08bca1f59442495bc5c01e2f0ba8c9079ca`

```dockerfile
```

-	Layers:
	-	`sha256:56e88217b045f05b58b9caa245c23fded45cf4a2be1d1c230f34b1b574fb44e4`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:501e68fff243f1b20a14eb50b92274eb17d3668b18614971adbe63c11f567f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82330387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee568acabd5eb2489c8492d7ccfa16f09434e29b4969f6f9772f2e41aa022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b78442a5d78ba9003dcc9cdc85c9df4f9cfafb1ad42b203d6ac1ea49040aab4`  
		Last Modified: Tue, 13 May 2025 23:48:04 GMT  
		Size: 78.9 MB (78864705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b116832fccbcf9a985576f61c96fe8c6bd152de5d63b1d3584e815df6cc8030`  
		Last Modified: Thu, 15 May 2025 20:15:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004edc5aa7acec0262bd1823f0da31ecb8e70efaf37858b2ea6ca28bf441780e`  
		Last Modified: Thu, 15 May 2025 20:21:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09e44671e22716a149f4d002f38e34628f91c212ba0e3057686c99a07ab0e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286f1515be59ef428b8da884b540ac598ed7f2a8b8e6f64ea9635f564882715`

```dockerfile
```

-	Layers:
	-	`sha256:725f13bcaad1fad6dc735aa5a28fbbe6d5b682b7282865560844161fc6878b0b`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f71a73be8317c4072b991ee98c4c3d8eadb24d188800178968beb834c5724d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76254322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39867711695ca6650e67c074879731c99cebcdfc99080d153b82a437bbd0c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9b258186a0fcc1c5c8c94beeb1d5bb81c0ab46f616ce67e7a00bf431cc4a3`  
		Last Modified: Wed, 14 May 2025 00:00:26 GMT  
		Size: 72.7 MB (72677915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e89d21db4cd9964b28450f72cf636a52889cfe69f1d4cb2f242a5a3d2ad350`  
		Last Modified: Thu, 15 May 2025 20:15:42 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b02ea0fef7a75f4975001831e3cc80c4fc8904726393c3c240acce25932a96`  
		Last Modified: Thu, 15 May 2025 20:20:52 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b8bb1c1c7e7e8608aacbef7f0b606beb2db199da80c18d189ad22ba69cf00370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6951c078ba75ba3eb2418cecd3a1e5b91a4373905eabd1a4d5caee74b8d56e9`

```dockerfile
```

-	Layers:
	-	`sha256:cfc6a58d241c77836c04f39e0e1a7adfe81d3ee28a3f7889eec06d865211a268`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:01893f1c5743b8d2b36383618902945cba7b093649f09519ebe158ba9f5f8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70859326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd196cc640f60dfe5eaa365485db2e8c6aac01a37f71995a8895ac495f0e5587`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58c2794411aa50dc12dbb79cdf53b10c92442248361dbe2644b83e7d4d2ba`  
		Last Modified: Tue, 13 May 2025 23:56:19 GMT  
		Size: 67.4 MB (67389700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824335bb1eb8cfc81d98eb1052441a94a5806fa9e3d060cb71f520520d0bf74`  
		Last Modified: Thu, 15 May 2025 20:22:31 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31dbfe4dde5d97940cea5e1c9a3d64dbc3d17c8aaba5d04926e5a54fe250069`  
		Last Modified: Thu, 15 May 2025 20:26:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82c172006540f09f9dd5322d8d9f23fda47f1ad037a7196f60115a40f504927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75b90bd5fa7d9fccf356e10d78df6ec4e00a7a88ad8dd24d0ec915d5e64412`

```dockerfile
```

-	Layers:
	-	`sha256:68c68e03488141b66b6f577ded0927247796d3cc30661286e556cf227077b16c`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:9f57aef81284589ae063257f9d0244ceb1bb0879cd2fff32f8ec9aa0c2432988
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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4fefe8df5fecde1f9ecc6cc1c8fd8495d0e29a9e789d8e378507e2dd8f08281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104795466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645913d2da4cac3db624dceb37107a3a6732846f012e52193ae21702359eb0e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9260a9093c169ff66cf07680f7ad29921302f6f7c787dbb6f11d2b5408e967a`  
		Last Modified: Tue, 01 Jul 2025 08:51:13 GMT  
		Size: 80.9 MB (80854679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f5e3e112086012e875c48625845ddcda86fda4b350488076bf70f2c0fb1db`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d2856fcfca49973626913facafc24d441c7d798e5bf45f8ade15a77fc5d3d`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:3014215753f651a12948038fcd94caa0e267fdc2d8c6127ea6811e9f4e5e8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8f3144bc7874e6dbcdadbab7304d4df71a31c3d5c7199b37203e37251692d`

```dockerfile
```

-	Layers:
	-	`sha256:7cee7041929ae490f77027772083670dd4e0d5b1b963788897ef9dea2d8b57f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:30 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b8ce72f9171467b5087f915e4724d198758a50f3600251f84ddc40415c2e6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128782240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28b0bd963eec8028fbcfd095410239bc81899873d9ac3993b8b00a4c005ee1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a36cfc1a32abdd38315b21dc7d982dc81502c01c3d731fcad2f110f057f37f`  
		Last Modified: Tue, 01 Jul 2025 06:49:21 GMT  
		Size: 100.7 MB (100702515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3386165ac1e78d913cca676585f17b3d3085d8d106771b0c95257dd19b211438`  
		Last Modified: Tue, 01 Jul 2025 06:48:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2b8fa324fd60ea700c3952a12505fe90202e805ea1acd941cb02a63766ca2`  
		Last Modified: Tue, 01 Jul 2025 06:48:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:2707221f195aa28c3f78132f6cc9c0fc292d52eb38cbb035988a91f49223823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cf22dae8faf4485734811bbe5474e1ab14bbb3430b3767f6d163715653049`

```dockerfile
```

-	Layers:
	-	`sha256:d940665171e4f9ebacd8803d861f792ef657925a7431742bb54ba647f2950894`  
		Last Modified: Tue, 01 Jul 2025 09:19:33 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; ppc64le

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

### `varnish:7.7` - unknown; unknown

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

### `varnish:7.7` - linux; s390x

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

### `varnish:7.7` - unknown; unknown

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

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:cc0a7aad884e7e86b751fbb031c56ebee7bef90fe3b05b3272aa58322bfe0af6
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
$ docker pull varnish@sha256:e68dc9857076551f8a67225317a95f345ad91e1f11c46c34210a7291adca6967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80315725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9095c515e21eb54100068f9a2ecfb3955655c2ee88fef95f72e3ccb6db24e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37e905a5b0a7e3887b2a91c8327b24129284a0d4f3951d3d9c1bc2c311a62d`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 76.7 MB (76671419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deacc4f5ce53935aa92bcf316166edecb88d737a471b0c6ca0bf48473cc100e`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d05040e8ab5a7400a08463a05466ce025243a468968194a57f9d867ed71c4`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:073fbd63633e8cfd353e4ec52c591ba2ac33e0e754cfb31912e3e78c8c0e2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23415dee6df89120996803f92b9564456f2f811d2762c918a334bafcdec5278`

```dockerfile
```

-	Layers:
	-	`sha256:018e7686fef92c81e6d79fd1f1bd13969950d4398f0435fad294561c8af9547a`  
		Last Modified: Wed, 04 Jun 2025 22:50:23 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:00ac6b75c1690c74500ec45b30a46a8760a81a908c866bff46a826f6d6d46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62366095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240af100b3925d63c86bcc69ff57620fcbc327ba2ba5ace25bb0e38926a2fdd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277c43e2a6e7ca8224b892d8251fd2f8944eb81fd376d90c5240f7816a0f083`  
		Last Modified: Thu, 03 Jul 2025 03:49:30 GMT  
		Size: 59.3 MB (59265914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd3f2d2fac3ed373219e2f04eb8c553a4b9cd07f49822a348cd6bd0ba0bf03`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107ef22442871d82b7ec5388ec01e3e2959a9e0e457bb531af8f317f1835928`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7350079942c472339e1816bfd7c6aedd38cc60d56c537313b4dd72db0413bc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a141db0e280fa2f137f3bd523ff5c2742c2efe54f70ea8fc5b7b2ed71f6168`

```dockerfile
```

-	Layers:
	-	`sha256:ca90931822ce458bc12a86e23a88bd82f7c8417c72e440a288c63ba1980187de`  
		Last Modified: Thu, 03 Jul 2025 03:50:35 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0f90786ecfa0f4e952a8bfcd7cf90ffb65f55afe12a1038b44d230554da349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77317664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a8e20c8b0476e94c93500537b71b2d6c9be6fbf759d39ebf428c5825cdf764`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84cd3f100e7a4987c9955b88d2ef87afc93a0e64cd6d8aa10263812165fe27`  
		Last Modified: Tue, 03 Jun 2025 14:12:57 GMT  
		Size: 73.3 MB (73322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f9e26ec65432a8efe09f77a816bf77b643748294604f7eeedb1601897d54`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204ee6311ecdf7dd9255ffe86d6389a3da94408d715faa19f1d7c770750e654`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1fc387008de696d9c88f44df0d8657685c27996c772c00f3d72fbf60635b7557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c364243c247b5f5a8019e10d2800233ed9c74c18cda92e040fcae27072732a`

```dockerfile
```

-	Layers:
	-	`sha256:9886a9295fbfcfb2c559ef20677457a21cea3b439be5bb62329e04ff2d942936`  
		Last Modified: Thu, 03 Jul 2025 03:51:56 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b121f54ac7f5b5c56b4247fd3a89f5eaa87edb49536a78080a31283009af079c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82508852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09ad2b11367485e00ad4bfd5a72c959b265f7da89c593cb821cd1bd3a31f35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c61829aa639dff24aad65e1a82bc8d02bf867875e2d4c5e53137c5276cb2d1`  
		Last Modified: Thu, 03 Jul 2025 03:52:07 GMT  
		Size: 79.0 MB (79043172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960eea97cf4f85503b6f86d972a55d352d8befc1bb5ce313e3afd030bde0419`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f18cbf086639292a7cf6ea4ef41ea5008005b3aaad98bac0c1e90b1d31838a`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d1466d9b377d819bd92e5f57939cb0c6d678cbfeda41f7364e267c23ad3635d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75d8d35091397ece88fcbfedf8015f162f250dfa08ba6c4d34d51e129502f7`

```dockerfile
```

-	Layers:
	-	`sha256:1acecb9b3a5cda019c5227afed2ea18570ffeaeb102971e5262e9ae248497b27`  
		Last Modified: Thu, 03 Jul 2025 03:53:16 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:71d583672fd210f53a87283c6cd7d8f0724cb438133803dcc2efddc983a4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76438752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9699c43a7e79fb04a4be6186b24690ad97f4e62825ee80eff8b1c7d7e0f210`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbab925e54587cbf4497c7970617c093c097ad8c8130f3f3683fca36278df31`  
		Last Modified: Thu, 03 Jul 2025 03:53:27 GMT  
		Size: 72.9 MB (72862344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb5bd15cbeac020aacb495032517a81a030115e97271921f08eb49865f0045`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b52ba2323f2f33051b67003e5f5ccb783f00ff3b7aa934e8d32dbea2c1860`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d94a917abc20ae0e4c8bc4e8f7f1d2945a698b16383f1f33a790aad4876148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c61ed2fadd3eb862006a0a17f29ccc99948148d5f87e0a3ee70403c5c3616c`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a360fb74bcf4bac9f6756708403acf376b869d1fb1bab0b248394b4b0fcfb`  
		Last Modified: Thu, 03 Jul 2025 03:54:30 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d11e359e354542668965c74d14c43927f83784083bff1786e638ab48d378112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73df919373dc10e0f84e083bf120e846c130d92fffa1442e1f8bc4441b7a7c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b83f7ad8b83b5dcd56c2bd88b05dac6dbb70832ec12eecc3357cf097f7557`  
		Last Modified: Thu, 03 Jul 2025 03:54:40 GMT  
		Size: 67.6 MB (67564885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacd333e5c4954b9a8d9f90265c801e8336cd7c6961afdc4b95da8145104dec`  
		Last Modified: Thu, 03 Jul 2025 03:55:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2611d5ee154f2c95fdcb474c498be2f8f0689c6c70cc4fa28acb770361e34fc`  
		Last Modified: Thu, 03 Jul 2025 03:55:40 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f1c5fa2662bf90956b5c270950cf6d6f2f8a1e3cf0aef9716aaa47400cc6afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188aab5b4924a51bfbd764a58d62bd7339a56f5b27faa5f8079ca6b60cf58257`

```dockerfile
```

-	Layers:
	-	`sha256:705f3871102b5aba5628f7eabccfed1d5bc984c5e7197744e5d5633ae2f279d5`  
		Last Modified: Thu, 03 Jul 2025 03:55:44 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.1`

```console
$ docker pull varnish@sha256:9f57aef81284589ae063257f9d0244ceb1bb0879cd2fff32f8ec9aa0c2432988
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

### `varnish:7.7.1` - linux; amd64

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

### `varnish:7.7.1` - unknown; unknown

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

### `varnish:7.7.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4fefe8df5fecde1f9ecc6cc1c8fd8495d0e29a9e789d8e378507e2dd8f08281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104795466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645913d2da4cac3db624dceb37107a3a6732846f012e52193ae21702359eb0e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9260a9093c169ff66cf07680f7ad29921302f6f7c787dbb6f11d2b5408e967a`  
		Last Modified: Tue, 01 Jul 2025 08:51:13 GMT  
		Size: 80.9 MB (80854679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f5e3e112086012e875c48625845ddcda86fda4b350488076bf70f2c0fb1db`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d2856fcfca49973626913facafc24d441c7d798e5bf45f8ade15a77fc5d3d`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:3014215753f651a12948038fcd94caa0e267fdc2d8c6127ea6811e9f4e5e8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8f3144bc7874e6dbcdadbab7304d4df71a31c3d5c7199b37203e37251692d`

```dockerfile
```

-	Layers:
	-	`sha256:7cee7041929ae490f77027772083670dd4e0d5b1b963788897ef9dea2d8b57f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:30 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b8ce72f9171467b5087f915e4724d198758a50f3600251f84ddc40415c2e6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128782240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28b0bd963eec8028fbcfd095410239bc81899873d9ac3993b8b00a4c005ee1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a36cfc1a32abdd38315b21dc7d982dc81502c01c3d731fcad2f110f057f37f`  
		Last Modified: Tue, 01 Jul 2025 06:49:21 GMT  
		Size: 100.7 MB (100702515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3386165ac1e78d913cca676585f17b3d3085d8d106771b0c95257dd19b211438`  
		Last Modified: Tue, 01 Jul 2025 06:48:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2b8fa324fd60ea700c3952a12505fe90202e805ea1acd941cb02a63766ca2`  
		Last Modified: Tue, 01 Jul 2025 06:48:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1` - unknown; unknown

```console
$ docker pull varnish@sha256:2707221f195aa28c3f78132f6cc9c0fc292d52eb38cbb035988a91f49223823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cf22dae8faf4485734811bbe5474e1ab14bbb3430b3767f6d163715653049`

```dockerfile
```

-	Layers:
	-	`sha256:d940665171e4f9ebacd8803d861f792ef657925a7431742bb54ba647f2950894`  
		Last Modified: Tue, 01 Jul 2025 09:19:33 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1` - linux; 386

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

### `varnish:7.7.1` - unknown; unknown

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

### `varnish:7.7.1` - linux; ppc64le

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

### `varnish:7.7.1` - unknown; unknown

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

### `varnish:7.7.1` - linux; s390x

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

### `varnish:7.7.1` - unknown; unknown

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

## `varnish:7.7.1-alpine`

```console
$ docker pull varnish@sha256:cc0a7aad884e7e86b751fbb031c56ebee7bef90fe3b05b3272aa58322bfe0af6
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

### `varnish:7.7.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:e68dc9857076551f8a67225317a95f345ad91e1f11c46c34210a7291adca6967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80315725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9095c515e21eb54100068f9a2ecfb3955655c2ee88fef95f72e3ccb6db24e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37e905a5b0a7e3887b2a91c8327b24129284a0d4f3951d3d9c1bc2c311a62d`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 76.7 MB (76671419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deacc4f5ce53935aa92bcf316166edecb88d737a471b0c6ca0bf48473cc100e`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d05040e8ab5a7400a08463a05466ce025243a468968194a57f9d867ed71c4`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:073fbd63633e8cfd353e4ec52c591ba2ac33e0e754cfb31912e3e78c8c0e2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23415dee6df89120996803f92b9564456f2f811d2762c918a334bafcdec5278`

```dockerfile
```

-	Layers:
	-	`sha256:018e7686fef92c81e6d79fd1f1bd13969950d4398f0435fad294561c8af9547a`  
		Last Modified: Wed, 04 Jun 2025 22:50:23 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:00ac6b75c1690c74500ec45b30a46a8760a81a908c866bff46a826f6d6d46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62366095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240af100b3925d63c86bcc69ff57620fcbc327ba2ba5ace25bb0e38926a2fdd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277c43e2a6e7ca8224b892d8251fd2f8944eb81fd376d90c5240f7816a0f083`  
		Last Modified: Thu, 03 Jul 2025 03:49:30 GMT  
		Size: 59.3 MB (59265914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd3f2d2fac3ed373219e2f04eb8c553a4b9cd07f49822a348cd6bd0ba0bf03`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107ef22442871d82b7ec5388ec01e3e2959a9e0e457bb531af8f317f1835928`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7350079942c472339e1816bfd7c6aedd38cc60d56c537313b4dd72db0413bc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a141db0e280fa2f137f3bd523ff5c2742c2efe54f70ea8fc5b7b2ed71f6168`

```dockerfile
```

-	Layers:
	-	`sha256:ca90931822ce458bc12a86e23a88bd82f7c8417c72e440a288c63ba1980187de`  
		Last Modified: Thu, 03 Jul 2025 03:50:35 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0f90786ecfa0f4e952a8bfcd7cf90ffb65f55afe12a1038b44d230554da349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77317664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a8e20c8b0476e94c93500537b71b2d6c9be6fbf759d39ebf428c5825cdf764`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84cd3f100e7a4987c9955b88d2ef87afc93a0e64cd6d8aa10263812165fe27`  
		Last Modified: Tue, 03 Jun 2025 14:12:57 GMT  
		Size: 73.3 MB (73322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f9e26ec65432a8efe09f77a816bf77b643748294604f7eeedb1601897d54`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204ee6311ecdf7dd9255ffe86d6389a3da94408d715faa19f1d7c770750e654`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1fc387008de696d9c88f44df0d8657685c27996c772c00f3d72fbf60635b7557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c364243c247b5f5a8019e10d2800233ed9c74c18cda92e040fcae27072732a`

```dockerfile
```

-	Layers:
	-	`sha256:9886a9295fbfcfb2c559ef20677457a21cea3b439be5bb62329e04ff2d942936`  
		Last Modified: Thu, 03 Jul 2025 03:51:56 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b121f54ac7f5b5c56b4247fd3a89f5eaa87edb49536a78080a31283009af079c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82508852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09ad2b11367485e00ad4bfd5a72c959b265f7da89c593cb821cd1bd3a31f35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c61829aa639dff24aad65e1a82bc8d02bf867875e2d4c5e53137c5276cb2d1`  
		Last Modified: Thu, 03 Jul 2025 03:52:07 GMT  
		Size: 79.0 MB (79043172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960eea97cf4f85503b6f86d972a55d352d8befc1bb5ce313e3afd030bde0419`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f18cbf086639292a7cf6ea4ef41ea5008005b3aaad98bac0c1e90b1d31838a`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d1466d9b377d819bd92e5f57939cb0c6d678cbfeda41f7364e267c23ad3635d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75d8d35091397ece88fcbfedf8015f162f250dfa08ba6c4d34d51e129502f7`

```dockerfile
```

-	Layers:
	-	`sha256:1acecb9b3a5cda019c5227afed2ea18570ffeaeb102971e5262e9ae248497b27`  
		Last Modified: Thu, 03 Jul 2025 03:53:16 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:71d583672fd210f53a87283c6cd7d8f0724cb438133803dcc2efddc983a4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76438752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9699c43a7e79fb04a4be6186b24690ad97f4e62825ee80eff8b1c7d7e0f210`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbab925e54587cbf4497c7970617c093c097ad8c8130f3f3683fca36278df31`  
		Last Modified: Thu, 03 Jul 2025 03:53:27 GMT  
		Size: 72.9 MB (72862344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb5bd15cbeac020aacb495032517a81a030115e97271921f08eb49865f0045`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b52ba2323f2f33051b67003e5f5ccb783f00ff3b7aa934e8d32dbea2c1860`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d94a917abc20ae0e4c8bc4e8f7f1d2945a698b16383f1f33a790aad4876148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c61ed2fadd3eb862006a0a17f29ccc99948148d5f87e0a3ee70403c5c3616c`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a360fb74bcf4bac9f6756708403acf376b869d1fb1bab0b248394b4b0fcfb`  
		Last Modified: Thu, 03 Jul 2025 03:54:30 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d11e359e354542668965c74d14c43927f83784083bff1786e638ab48d378112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73df919373dc10e0f84e083bf120e846c130d92fffa1442e1f8bc4441b7a7c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b83f7ad8b83b5dcd56c2bd88b05dac6dbb70832ec12eecc3357cf097f7557`  
		Last Modified: Thu, 03 Jul 2025 03:54:40 GMT  
		Size: 67.6 MB (67564885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacd333e5c4954b9a8d9f90265c801e8336cd7c6961afdc4b95da8145104dec`  
		Last Modified: Thu, 03 Jul 2025 03:55:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2611d5ee154f2c95fdcb474c498be2f8f0689c6c70cc4fa28acb770361e34fc`  
		Last Modified: Thu, 03 Jul 2025 03:55:40 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f1c5fa2662bf90956b5c270950cf6d6f2f8a1e3cf0aef9716aaa47400cc6afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188aab5b4924a51bfbd764a58d62bd7339a56f5b27faa5f8079ca6b60cf58257`

```dockerfile
```

-	Layers:
	-	`sha256:705f3871102b5aba5628f7eabccfed1d5bc984c5e7197744e5d5633ae2f279d5`  
		Last Modified: Thu, 03 Jul 2025 03:55:44 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:cc0a7aad884e7e86b751fbb031c56ebee7bef90fe3b05b3272aa58322bfe0af6
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
$ docker pull varnish@sha256:e68dc9857076551f8a67225317a95f345ad91e1f11c46c34210a7291adca6967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80315725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9095c515e21eb54100068f9a2ecfb3955655c2ee88fef95f72e3ccb6db24e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37e905a5b0a7e3887b2a91c8327b24129284a0d4f3951d3d9c1bc2c311a62d`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 76.7 MB (76671419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deacc4f5ce53935aa92bcf316166edecb88d737a471b0c6ca0bf48473cc100e`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d05040e8ab5a7400a08463a05466ce025243a468968194a57f9d867ed71c4`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:073fbd63633e8cfd353e4ec52c591ba2ac33e0e754cfb31912e3e78c8c0e2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23415dee6df89120996803f92b9564456f2f811d2762c918a334bafcdec5278`

```dockerfile
```

-	Layers:
	-	`sha256:018e7686fef92c81e6d79fd1f1bd13969950d4398f0435fad294561c8af9547a`  
		Last Modified: Wed, 04 Jun 2025 22:50:23 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:00ac6b75c1690c74500ec45b30a46a8760a81a908c866bff46a826f6d6d46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62366095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240af100b3925d63c86bcc69ff57620fcbc327ba2ba5ace25bb0e38926a2fdd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277c43e2a6e7ca8224b892d8251fd2f8944eb81fd376d90c5240f7816a0f083`  
		Last Modified: Thu, 03 Jul 2025 03:49:30 GMT  
		Size: 59.3 MB (59265914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd3f2d2fac3ed373219e2f04eb8c553a4b9cd07f49822a348cd6bd0ba0bf03`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107ef22442871d82b7ec5388ec01e3e2959a9e0e457bb531af8f317f1835928`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7350079942c472339e1816bfd7c6aedd38cc60d56c537313b4dd72db0413bc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a141db0e280fa2f137f3bd523ff5c2742c2efe54f70ea8fc5b7b2ed71f6168`

```dockerfile
```

-	Layers:
	-	`sha256:ca90931822ce458bc12a86e23a88bd82f7c8417c72e440a288c63ba1980187de`  
		Last Modified: Thu, 03 Jul 2025 03:50:35 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0f90786ecfa0f4e952a8bfcd7cf90ffb65f55afe12a1038b44d230554da349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77317664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a8e20c8b0476e94c93500537b71b2d6c9be6fbf759d39ebf428c5825cdf764`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84cd3f100e7a4987c9955b88d2ef87afc93a0e64cd6d8aa10263812165fe27`  
		Last Modified: Tue, 03 Jun 2025 14:12:57 GMT  
		Size: 73.3 MB (73322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f9e26ec65432a8efe09f77a816bf77b643748294604f7eeedb1601897d54`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204ee6311ecdf7dd9255ffe86d6389a3da94408d715faa19f1d7c770750e654`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1fc387008de696d9c88f44df0d8657685c27996c772c00f3d72fbf60635b7557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c364243c247b5f5a8019e10d2800233ed9c74c18cda92e040fcae27072732a`

```dockerfile
```

-	Layers:
	-	`sha256:9886a9295fbfcfb2c559ef20677457a21cea3b439be5bb62329e04ff2d942936`  
		Last Modified: Thu, 03 Jul 2025 03:51:56 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:b121f54ac7f5b5c56b4247fd3a89f5eaa87edb49536a78080a31283009af079c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82508852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09ad2b11367485e00ad4bfd5a72c959b265f7da89c593cb821cd1bd3a31f35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c61829aa639dff24aad65e1a82bc8d02bf867875e2d4c5e53137c5276cb2d1`  
		Last Modified: Thu, 03 Jul 2025 03:52:07 GMT  
		Size: 79.0 MB (79043172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960eea97cf4f85503b6f86d972a55d352d8befc1bb5ce313e3afd030bde0419`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f18cbf086639292a7cf6ea4ef41ea5008005b3aaad98bac0c1e90b1d31838a`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d1466d9b377d819bd92e5f57939cb0c6d678cbfeda41f7364e267c23ad3635d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75d8d35091397ece88fcbfedf8015f162f250dfa08ba6c4d34d51e129502f7`

```dockerfile
```

-	Layers:
	-	`sha256:1acecb9b3a5cda019c5227afed2ea18570ffeaeb102971e5262e9ae248497b27`  
		Last Modified: Thu, 03 Jul 2025 03:53:16 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:71d583672fd210f53a87283c6cd7d8f0724cb438133803dcc2efddc983a4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76438752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9699c43a7e79fb04a4be6186b24690ad97f4e62825ee80eff8b1c7d7e0f210`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbab925e54587cbf4497c7970617c093c097ad8c8130f3f3683fca36278df31`  
		Last Modified: Thu, 03 Jul 2025 03:53:27 GMT  
		Size: 72.9 MB (72862344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb5bd15cbeac020aacb495032517a81a030115e97271921f08eb49865f0045`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b52ba2323f2f33051b67003e5f5ccb783f00ff3b7aa934e8d32dbea2c1860`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d94a917abc20ae0e4c8bc4e8f7f1d2945a698b16383f1f33a790aad4876148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c61ed2fadd3eb862006a0a17f29ccc99948148d5f87e0a3ee70403c5c3616c`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a360fb74bcf4bac9f6756708403acf376b869d1fb1bab0b248394b4b0fcfb`  
		Last Modified: Thu, 03 Jul 2025 03:54:30 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d11e359e354542668965c74d14c43927f83784083bff1786e638ab48d378112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73df919373dc10e0f84e083bf120e846c130d92fffa1442e1f8bc4441b7a7c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b83f7ad8b83b5dcd56c2bd88b05dac6dbb70832ec12eecc3357cf097f7557`  
		Last Modified: Thu, 03 Jul 2025 03:54:40 GMT  
		Size: 67.6 MB (67564885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacd333e5c4954b9a8d9f90265c801e8336cd7c6961afdc4b95da8145104dec`  
		Last Modified: Thu, 03 Jul 2025 03:55:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2611d5ee154f2c95fdcb474c498be2f8f0689c6c70cc4fa28acb770361e34fc`  
		Last Modified: Thu, 03 Jul 2025 03:55:40 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f1c5fa2662bf90956b5c270950cf6d6f2f8a1e3cf0aef9716aaa47400cc6afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188aab5b4924a51bfbd764a58d62bd7339a56f5b27faa5f8079ca6b60cf58257`

```dockerfile
```

-	Layers:
	-	`sha256:705f3871102b5aba5628f7eabccfed1d5bc984c5e7197744e5d5633ae2f279d5`  
		Last Modified: Thu, 03 Jul 2025 03:55:44 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:9f57aef81284589ae063257f9d0244ceb1bb0879cd2fff32f8ec9aa0c2432988
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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4fefe8df5fecde1f9ecc6cc1c8fd8495d0e29a9e789d8e378507e2dd8f08281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104795466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645913d2da4cac3db624dceb37107a3a6732846f012e52193ae21702359eb0e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9260a9093c169ff66cf07680f7ad29921302f6f7c787dbb6f11d2b5408e967a`  
		Last Modified: Tue, 01 Jul 2025 08:51:13 GMT  
		Size: 80.9 MB (80854679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f5e3e112086012e875c48625845ddcda86fda4b350488076bf70f2c0fb1db`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d2856fcfca49973626913facafc24d441c7d798e5bf45f8ade15a77fc5d3d`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:3014215753f651a12948038fcd94caa0e267fdc2d8c6127ea6811e9f4e5e8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8f3144bc7874e6dbcdadbab7304d4df71a31c3d5c7199b37203e37251692d`

```dockerfile
```

-	Layers:
	-	`sha256:7cee7041929ae490f77027772083670dd4e0d5b1b963788897ef9dea2d8b57f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:30 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b8ce72f9171467b5087f915e4724d198758a50f3600251f84ddc40415c2e6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128782240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28b0bd963eec8028fbcfd095410239bc81899873d9ac3993b8b00a4c005ee1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a36cfc1a32abdd38315b21dc7d982dc81502c01c3d731fcad2f110f057f37f`  
		Last Modified: Tue, 01 Jul 2025 06:49:21 GMT  
		Size: 100.7 MB (100702515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3386165ac1e78d913cca676585f17b3d3085d8d106771b0c95257dd19b211438`  
		Last Modified: Tue, 01 Jul 2025 06:48:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2b8fa324fd60ea700c3952a12505fe90202e805ea1acd941cb02a63766ca2`  
		Last Modified: Tue, 01 Jul 2025 06:48:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:2707221f195aa28c3f78132f6cc9c0fc292d52eb38cbb035988a91f49223823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cf22dae8faf4485734811bbe5474e1ab14bbb3430b3767f6d163715653049`

```dockerfile
```

-	Layers:
	-	`sha256:d940665171e4f9ebacd8803d861f792ef657925a7431742bb54ba647f2950894`  
		Last Modified: Tue, 01 Jul 2025 09:19:33 GMT  
		Size: 19.5 KB (19548 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; ppc64le

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

### `varnish:fresh` - unknown; unknown

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

### `varnish:fresh` - linux; s390x

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

### `varnish:fresh` - unknown; unknown

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

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:cc0a7aad884e7e86b751fbb031c56ebee7bef90fe3b05b3272aa58322bfe0af6
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
$ docker pull varnish@sha256:e68dc9857076551f8a67225317a95f345ad91e1f11c46c34210a7291adca6967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80315725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9095c515e21eb54100068f9a2ecfb3955655c2ee88fef95f72e3ccb6db24e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37e905a5b0a7e3887b2a91c8327b24129284a0d4f3951d3d9c1bc2c311a62d`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 76.7 MB (76671419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deacc4f5ce53935aa92bcf316166edecb88d737a471b0c6ca0bf48473cc100e`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d05040e8ab5a7400a08463a05466ce025243a468968194a57f9d867ed71c4`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:073fbd63633e8cfd353e4ec52c591ba2ac33e0e754cfb31912e3e78c8c0e2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23415dee6df89120996803f92b9564456f2f811d2762c918a334bafcdec5278`

```dockerfile
```

-	Layers:
	-	`sha256:018e7686fef92c81e6d79fd1f1bd13969950d4398f0435fad294561c8af9547a`  
		Last Modified: Wed, 04 Jun 2025 22:50:23 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:00ac6b75c1690c74500ec45b30a46a8760a81a908c866bff46a826f6d6d46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62366095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240af100b3925d63c86bcc69ff57620fcbc327ba2ba5ace25bb0e38926a2fdd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277c43e2a6e7ca8224b892d8251fd2f8944eb81fd376d90c5240f7816a0f083`  
		Last Modified: Thu, 03 Jul 2025 03:49:30 GMT  
		Size: 59.3 MB (59265914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd3f2d2fac3ed373219e2f04eb8c553a4b9cd07f49822a348cd6bd0ba0bf03`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107ef22442871d82b7ec5388ec01e3e2959a9e0e457bb531af8f317f1835928`  
		Last Modified: Sat, 14 Jun 2025 10:02:07 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7350079942c472339e1816bfd7c6aedd38cc60d56c537313b4dd72db0413bc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a141db0e280fa2f137f3bd523ff5c2742c2efe54f70ea8fc5b7b2ed71f6168`

```dockerfile
```

-	Layers:
	-	`sha256:ca90931822ce458bc12a86e23a88bd82f7c8417c72e440a288c63ba1980187de`  
		Last Modified: Thu, 03 Jul 2025 03:50:35 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0f90786ecfa0f4e952a8bfcd7cf90ffb65f55afe12a1038b44d230554da349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77317664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a8e20c8b0476e94c93500537b71b2d6c9be6fbf759d39ebf428c5825cdf764`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84cd3f100e7a4987c9955b88d2ef87afc93a0e64cd6d8aa10263812165fe27`  
		Last Modified: Tue, 03 Jun 2025 14:12:57 GMT  
		Size: 73.3 MB (73322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f9e26ec65432a8efe09f77a816bf77b643748294604f7eeedb1601897d54`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204ee6311ecdf7dd9255ffe86d6389a3da94408d715faa19f1d7c770750e654`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1fc387008de696d9c88f44df0d8657685c27996c772c00f3d72fbf60635b7557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c364243c247b5f5a8019e10d2800233ed9c74c18cda92e040fcae27072732a`

```dockerfile
```

-	Layers:
	-	`sha256:9886a9295fbfcfb2c559ef20677457a21cea3b439be5bb62329e04ff2d942936`  
		Last Modified: Thu, 03 Jul 2025 03:51:56 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b121f54ac7f5b5c56b4247fd3a89f5eaa87edb49536a78080a31283009af079c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82508852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09ad2b11367485e00ad4bfd5a72c959b265f7da89c593cb821cd1bd3a31f35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c61829aa639dff24aad65e1a82bc8d02bf867875e2d4c5e53137c5276cb2d1`  
		Last Modified: Thu, 03 Jul 2025 03:52:07 GMT  
		Size: 79.0 MB (79043172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960eea97cf4f85503b6f86d972a55d352d8befc1bb5ce313e3afd030bde0419`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f18cbf086639292a7cf6ea4ef41ea5008005b3aaad98bac0c1e90b1d31838a`  
		Last Modified: Sat, 07 Jun 2025 06:39:46 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d1466d9b377d819bd92e5f57939cb0c6d678cbfeda41f7364e267c23ad3635d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75d8d35091397ece88fcbfedf8015f162f250dfa08ba6c4d34d51e129502f7`

```dockerfile
```

-	Layers:
	-	`sha256:1acecb9b3a5cda019c5227afed2ea18570ffeaeb102971e5262e9ae248497b27`  
		Last Modified: Thu, 03 Jul 2025 03:53:16 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:71d583672fd210f53a87283c6cd7d8f0724cb438133803dcc2efddc983a4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76438752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9699c43a7e79fb04a4be6186b24690ad97f4e62825ee80eff8b1c7d7e0f210`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbab925e54587cbf4497c7970617c093c097ad8c8130f3f3683fca36278df31`  
		Last Modified: Thu, 03 Jul 2025 03:53:27 GMT  
		Size: 72.9 MB (72862344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb5bd15cbeac020aacb495032517a81a030115e97271921f08eb49865f0045`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b52ba2323f2f33051b67003e5f5ccb783f00ff3b7aa934e8d32dbea2c1860`  
		Last Modified: Sun, 15 Jun 2025 18:08:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d94a917abc20ae0e4c8bc4e8f7f1d2945a698b16383f1f33a790aad4876148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c61ed2fadd3eb862006a0a17f29ccc99948148d5f87e0a3ee70403c5c3616c`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a360fb74bcf4bac9f6756708403acf376b869d1fb1bab0b248394b4b0fcfb`  
		Last Modified: Thu, 03 Jul 2025 03:54:30 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d11e359e354542668965c74d14c43927f83784083bff1786e638ab48d378112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73df919373dc10e0f84e083bf120e846c130d92fffa1442e1f8bc4441b7a7c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
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
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b83f7ad8b83b5dcd56c2bd88b05dac6dbb70832ec12eecc3357cf097f7557`  
		Last Modified: Thu, 03 Jul 2025 03:54:40 GMT  
		Size: 67.6 MB (67564885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacd333e5c4954b9a8d9f90265c801e8336cd7c6961afdc4b95da8145104dec`  
		Last Modified: Thu, 03 Jul 2025 03:55:39 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2611d5ee154f2c95fdcb474c498be2f8f0689c6c70cc4fa28acb770361e34fc`  
		Last Modified: Thu, 03 Jul 2025 03:55:40 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f1c5fa2662bf90956b5c270950cf6d6f2f8a1e3cf0aef9716aaa47400cc6afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188aab5b4924a51bfbd764a58d62bd7339a56f5b27faa5f8079ca6b60cf58257`

```dockerfile
```

-	Layers:
	-	`sha256:705f3871102b5aba5628f7eabccfed1d5bc984c5e7197744e5d5633ae2f279d5`  
		Last Modified: Thu, 03 Jul 2025 03:55:44 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:9f57aef81284589ae063257f9d0244ceb1bb0879cd2fff32f8ec9aa0c2432988
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
$ docker pull varnish@sha256:4fefe8df5fecde1f9ecc6cc1c8fd8495d0e29a9e789d8e378507e2dd8f08281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104795466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645913d2da4cac3db624dceb37107a3a6732846f012e52193ae21702359eb0e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9260a9093c169ff66cf07680f7ad29921302f6f7c787dbb6f11d2b5408e967a`  
		Last Modified: Tue, 01 Jul 2025 08:51:13 GMT  
		Size: 80.9 MB (80854679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f5e3e112086012e875c48625845ddcda86fda4b350488076bf70f2c0fb1db`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d2856fcfca49973626913facafc24d441c7d798e5bf45f8ade15a77fc5d3d`  
		Last Modified: Tue, 01 Jul 2025 08:51:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:3014215753f651a12948038fcd94caa0e267fdc2d8c6127ea6811e9f4e5e8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8f3144bc7874e6dbcdadbab7304d4df71a31c3d5c7199b37203e37251692d`

```dockerfile
```

-	Layers:
	-	`sha256:7cee7041929ae490f77027772083670dd4e0d5b1b963788897ef9dea2d8b57f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:30 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b8ce72f9171467b5087f915e4724d198758a50f3600251f84ddc40415c2e6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128782240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28b0bd963eec8028fbcfd095410239bc81899873d9ac3993b8b00a4c005ee1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 26 May 2025 12:40:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a36cfc1a32abdd38315b21dc7d982dc81502c01c3d731fcad2f110f057f37f`  
		Last Modified: Tue, 01 Jul 2025 06:49:21 GMT  
		Size: 100.7 MB (100702515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3386165ac1e78d913cca676585f17b3d3085d8d106771b0c95257dd19b211438`  
		Last Modified: Tue, 01 Jul 2025 06:48:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2b8fa324fd60ea700c3952a12505fe90202e805ea1acd941cb02a63766ca2`  
		Last Modified: Tue, 01 Jul 2025 06:48:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:2707221f195aa28c3f78132f6cc9c0fc292d52eb38cbb035988a91f49223823d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cf22dae8faf4485734811bbe5474e1ab14bbb3430b3767f6d163715653049`

```dockerfile
```

-	Layers:
	-	`sha256:d940665171e4f9ebacd8803d861f792ef657925a7431742bb54ba647f2950894`  
		Last Modified: Tue, 01 Jul 2025 09:19:33 GMT  
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

## `varnish:old`

```console
$ docker pull varnish@sha256:f29b8e672ee825ce9e1c140af30692d2861785d45598709a7fdabe14736fb847
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
$ docker pull varnish@sha256:a07aff90a2582813f488b78a2cfa19e94533b92795fb2a8244a88875316774cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134236559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc048330b90e42aaddb7790bfa04d84fe03c492eca052304a25accff377353b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0891dd165e99b1eeb33af028ca85c451665cab5dfad0dc64f62b095d3b3aaf6e`  
		Last Modified: Tue, 01 Jul 2025 02:27:47 GMT  
		Size: 106.0 MB (106004377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c7ea422e8b12db1fbbc1cf1a306e02b5920b4838b917ccee0ed8d084e6fd9e`  
		Last Modified: Tue, 01 Jul 2025 02:27:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61655fca1b3e119f885d50ef25e5aebf9983ca4e15a6948c60c71d869830d51e`  
		Last Modified: Tue, 01 Jul 2025 02:27:32 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:6111454f49c12594f4f561fd3cb8d7e276c8f627d29ed03c5b002f5c5bfae6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af92e5ec85c0a42ea6fb924b8d704003a5c3ce62b4c3dfeea90e6e5772301940`

```dockerfile
```

-	Layers:
	-	`sha256:b728358d599001cb63131dd0187e0f00e591734d0a0585599900399e9870db0b`  
		Last Modified: Tue, 01 Jul 2025 06:19:54 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:da73f1c62c251a64681e9b0fc6bbfecfb6deb90cb3a047fe13b4442954055e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104595629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568675fe6f88f6af128d414ac2f5696675d4d75c148439bd2720000a8d98a65c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6458e3abbb227c914e1a49bee2e4f51c15ae4b98536784a041989965ac9ba1`  
		Last Modified: Tue, 01 Jul 2025 08:54:37 GMT  
		Size: 80.7 MB (80654837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024765d4f507e1d448078f2ff108b09cb0cef092c51642ae9211ce0a287ee29f`  
		Last Modified: Tue, 01 Jul 2025 08:54:30 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923df3354dd245a18916c4c74165caacd4c7de9994df44a6f9c29c8c66dd5f30`  
		Last Modified: Tue, 01 Jul 2025 08:54:30 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:abf0bb1c6aa0f2a0aeaa02a82a66856b2ae7b9815460c7132705d4d64989189c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e55b80eeee1f9fc1312c99d8c706e7dc642da4ad77c9b11818b9d8d412964`

```dockerfile
```

-	Layers:
	-	`sha256:59217e4edfc13af6b706ecacce82c23f7f84311c21c96fbf965dbb4e5e5c979e`  
		Last Modified: Tue, 01 Jul 2025 09:19:39 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2c9176807cb717e08edeaedf06863fe899b2d3d467a68eac824ae3e8843115a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128572969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef59fc06dbb57e6c0774103450f2ddf98ad6cc77f2d531df9070c294828573f9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e83a9c02989fa1f23897fd29799a0b7b2d3bff0e00ee8695c282d8bce3a242`  
		Last Modified: Tue, 01 Jul 2025 06:51:28 GMT  
		Size: 100.5 MB (100493245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16c098d7835542322bf64895feb17747c337fbd88c5485ca6fb78efe05ccf2`  
		Last Modified: Tue, 01 Jul 2025 06:51:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66b57aa3ca84bf7af5702d3cf511afb9699705e894837f7c14452ff16a587f6`  
		Last Modified: Tue, 01 Jul 2025 06:51:23 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:989bc63306ee66c9685a7d48d4142f1cf737b828277fdba121e829ec61d0f7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d00b20f9917fb609d9bc6fe50c727abb839ee7850e3aeb63832d7eb7033047`

```dockerfile
```

-	Layers:
	-	`sha256:97406f57931533547a7e3e141bfcd9ec9a7ae289e06bc677ca7a8a68a75475db`  
		Last Modified: Tue, 01 Jul 2025 09:19:42 GMT  
		Size: 18.9 KB (18939 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:84847ab9ccd5263018f014b382c13955fe1cc0c9b1a86d681971bdfba0de396a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131369924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24026a222474b539b5fc5edd99e115bf9523b5200b7a61f360c5db336052a42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc201735ad38a34f7d5941fc5f8e6e60bc0d0788c3ccbe7410436d553aea07`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 102.2 MB (102155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691102731be20916f7fe89899c11fc5ba76a2125f540757cc1be3c7c75caa183`  
		Last Modified: Tue, 01 Jul 2025 02:27:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f19e2f6820f0f2da871a873a709d4c67a4896adda3aca3cb98e1fa60687712`  
		Last Modified: Tue, 01 Jul 2025 02:27:18 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:7b6f92667483bfbd6210215a2587d693e6bce569b9ddb727cedc06fcee253a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5622681e44babbab58efeb45865ee0d5f5b0d125071a8d0f0239c423d107e9`

```dockerfile
```

-	Layers:
	-	`sha256:fd7721d58c7f4bf5b7192725c7a087aa85ad66aaf0c7354caeb41709c5adfda0`  
		Last Modified: Tue, 01 Jul 2025 06:20:05 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:02a913b6eacdf1f73d365966758b470e9c83d82bbc29d051f3c744018494bf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137051120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec4009d395c697dd2483d65780aca3c111425d0d442bdd5cd97f59d87db5fda`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96efbee2c552a9cf474e05a34f3262b0646bdf50fb24c73dc5492ebfe7c6f55f`  
		Last Modified: Tue, 01 Jul 2025 05:02:18 GMT  
		Size: 105.0 MB (104976253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7897143b748b83eb00fb95941d339eee8ff4dca883cdcb08c15fd0dadf9b3c`  
		Last Modified: Tue, 01 Jul 2025 05:02:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865829d57248d93931e9aeb809eaef2a3de0f94c66def6fb0bcfec1431b18991`  
		Last Modified: Tue, 01 Jul 2025 05:02:12 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:0dae0834473849a40c76a068d13890ace8f971d4cbde19d19b3fdee2ffe24e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81dadbef890e2d2483a97d716f001299537d461cdc7b355705b5ec2e90aa491`

```dockerfile
```

-	Layers:
	-	`sha256:a096e433f15d58b286f6f1cd45384cf1307798a8058cf30228a5fafe1e7ffd96`  
		Last Modified: Tue, 01 Jul 2025 06:20:08 GMT  
		Size: 18.9 KB (18885 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:d75dfa792b2c3979f84f6a00ae9c604ce8cdd63c49035cccde96fec2d396a73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112154499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b762437511e13ce33d1ce9e0d1fec726e3deda2822a4810a86c1017858bd739`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df2af803aa4e058f2551625308c7bb768a5a05ca93d14c6b813a07614ea8e0`  
		Last Modified: Tue, 01 Jul 2025 05:30:00 GMT  
		Size: 85.3 MB (85264642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdb789262a66091a769d34bc03648f88a07516966a157555ba43792771d9ba2`  
		Last Modified: Tue, 01 Jul 2025 05:29:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c269b94e20d7e9081e9bfb22d164a943cbdeeae12bc3971d32837b846590b1f7`  
		Last Modified: Tue, 01 Jul 2025 05:29:56 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:1cef0831a5e455416dadba79fef6302d40425187a7cc10a78f9cd82bcd3023e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b27bdee97d78442609432a7107ec22559cab4b6b79220ce79c5e831b9d90c4`

```dockerfile
```

-	Layers:
	-	`sha256:5f37e177e2913803da34c7c1a57ce635021502dac0f2471ecde5927420dce122`  
		Last Modified: Tue, 01 Jul 2025 06:20:12 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:cb268b57c8a2cec3d39e8e4f74382646c8795718ff25aa57c0d0a5ee3eb1146f
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
$ docker pull varnish@sha256:832539f3c49155c868d6e605b23d11635697ee79308d4d67632bfd80a3592470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef6a698cd1a97012baa9bdd2db973a223ae7b7500b68afd5d7a2849cffaf42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd875d896754e31f106b279b13f6496adc8421db2c4f87731e3e4723097d55`  
		Last Modified: Fri, 16 May 2025 13:21:30 GMT  
		Size: 76.5 MB (76480503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e6d4496a56a4cdc28e0728f444aca412abcdbf44de2a17517f260143d2445`  
		Last Modified: Thu, 15 May 2025 20:16:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2dce4d3db4cb8f19e79b85dd340da315f5a6503c0177d857e7d710bad2e19`  
		Last Modified: Thu, 15 May 2025 20:24:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:745b542be3ade7260c951fd0df6eb7803b1d483c633be4bbe214419631ee5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbc11303947e59091cf3071eab27aa971a25b9b73cfbb7832b60329497a50ab`

```dockerfile
```

-	Layers:
	-	`sha256:f89f56e4fa97bf3b52dbeb162f579e87f78751ccf4665eafdf273436ff4d5639`  
		Last Modified: Wed, 04 Jun 2025 22:49:56 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c6f15a90cf4d116fb28f39ecb012995aefb0ecd49c02fa0bd9aeec4adf65cebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348b5a86113885af2ad1ae03b67a656675d858bac28550d8756c22fb352073a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b64d240de8405e58901ffaa351cf6d995f373610fee29e4806ebafbe8f51b4`  
		Last Modified: Tue, 13 May 2025 23:54:33 GMT  
		Size: 59.1 MB (59076980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f345bef6ca24ad7825007178523af189952fa489de9d8eb18ddad503404c52e`  
		Last Modified: Thu, 15 May 2025 20:17:20 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb03c9836d2f802ac7a200af8b7b5a3d37f070eb40a1fca06426d08cf583d3`  
		Last Modified: Thu, 15 May 2025 20:27:18 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:341536aa96b8653cdc7655ab75a700a74a413abb92fbd62c9736a51d288996b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ccd8901dac22a6fcb8114bc93626ea4a138d3c97c173fc51ce70e0fff5f590`

```dockerfile
```

-	Layers:
	-	`sha256:9df71e7bf646620391b06844710aa5d6a127203721dbbdce0a0b070fe4301319`  
		Last Modified: Tue, 13 May 2025 23:54:31 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:03050dcb8e1b8c436dd6bb97d15cd02ce355fb92d5b0f4fd2a9d87236bacd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12c01235c01884aba1beb3ce7e3764811403422085d6361e69b7f7e89a142`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d0112c73e93ba409991084c46b91c454e8873ad85d1a0c704da073c738110`  
		Last Modified: Fri, 16 May 2025 20:41:39 GMT  
		Size: 73.1 MB (73139804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5db8d46da3afc53cd359504e09f6a3822ceefd1859d19b3d76bcffdefa2e7`  
		Last Modified: Thu, 15 May 2025 20:29:37 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afac65ae6f31067843e3de68aa1266f07ddce142c1ae08692d23030bee350b`  
		Last Modified: Thu, 15 May 2025 20:23:07 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:79357498a90f86e478600efa6dccae02abc17f66981aec1940ea28ced6fd52f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d5e0e50d45a1f2ae76d217647b08bca1f59442495bc5c01e2f0ba8c9079ca`

```dockerfile
```

-	Layers:
	-	`sha256:56e88217b045f05b58b9caa245c23fded45cf4a2be1d1c230f34b1b574fb44e4`  
		Last Modified: Tue, 13 May 2025 23:53:44 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:501e68fff243f1b20a14eb50b92274eb17d3668b18614971adbe63c11f567f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82330387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ee568acabd5eb2489c8492d7ccfa16f09434e29b4969f6f9772f2e41aa022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b78442a5d78ba9003dcc9cdc85c9df4f9cfafb1ad42b203d6ac1ea49040aab4`  
		Last Modified: Tue, 13 May 2025 23:48:04 GMT  
		Size: 78.9 MB (78864705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b116832fccbcf9a985576f61c96fe8c6bd152de5d63b1d3584e815df6cc8030`  
		Last Modified: Thu, 15 May 2025 20:15:44 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004edc5aa7acec0262bd1823f0da31ecb8e70efaf37858b2ea6ca28bf441780e`  
		Last Modified: Thu, 15 May 2025 20:21:59 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09e44671e22716a149f4d002f38e34628f91c212ba0e3057686c99a07ab0e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286f1515be59ef428b8da884b540ac598ed7f2a8b8e6f64ea9635f564882715`

```dockerfile
```

-	Layers:
	-	`sha256:725f13bcaad1fad6dc735aa5a28fbbe6d5b682b7282865560844161fc6878b0b`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:f71a73be8317c4072b991ee98c4c3d8eadb24d188800178968beb834c5724d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76254322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae39867711695ca6650e67c074879731c99cebcdfc99080d153b82a437bbd0c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9b258186a0fcc1c5c8c94beeb1d5bb81c0ab46f616ce67e7a00bf431cc4a3`  
		Last Modified: Wed, 14 May 2025 00:00:26 GMT  
		Size: 72.7 MB (72677915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e89d21db4cd9964b28450f72cf636a52889cfe69f1d4cb2f242a5a3d2ad350`  
		Last Modified: Thu, 15 May 2025 20:15:42 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b02ea0fef7a75f4975001831e3cc80c4fc8904726393c3c240acce25932a96`  
		Last Modified: Thu, 15 May 2025 20:20:52 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b8bb1c1c7e7e8608aacbef7f0b606beb2db199da80c18d189ad22ba69cf00370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6951c078ba75ba3eb2418cecd3a1e5b91a4373905eabd1a4d5caee74b8d56e9`

```dockerfile
```

-	Layers:
	-	`sha256:cfc6a58d241c77836c04f39e0e1a7adfe81d3ee28a3f7889eec06d865211a268`  
		Last Modified: Wed, 14 May 2025 00:00:24 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:01893f1c5743b8d2b36383618902945cba7b093649f09519ebe158ba9f5f8b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70859326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd196cc640f60dfe5eaa365485db2e8c6aac01a37f71995a8895ac495f0e5587`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=7.6.3
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 13 May 2025 22:18:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 13 May 2025 22:18:23 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 13 May 2025 22:18:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
ENV VSM_NOPID=1
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.3 DIST_SHA512=1d247ea4521a1bf0ea9b81f95d9b7d3df1f40da84ab0f0e3c47ce33553394549bafdc79d3dd6be044f3a3d2275db97595b57fb67c11f5922a6b200497016bf08 VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
USER varnish
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb58c2794411aa50dc12dbb79cdf53b10c92442248361dbe2644b83e7d4d2ba`  
		Last Modified: Tue, 13 May 2025 23:56:19 GMT  
		Size: 67.4 MB (67389700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a824335bb1eb8cfc81d98eb1052441a94a5806fa9e3d060cb71f520520d0bf74`  
		Last Modified: Thu, 15 May 2025 20:22:31 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31dbfe4dde5d97940cea5e1c9a3d64dbc3d17c8aaba5d04926e5a54fe250069`  
		Last Modified: Thu, 15 May 2025 20:26:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82c172006540f09f9dd5322d8d9f23fda47f1ad037a7196f60115a40f504927d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75b90bd5fa7d9fccf356e10d78df6ec4e00a7a88ad8dd24d0ec915d5e64412`

```dockerfile
```

-	Layers:
	-	`sha256:68c68e03488141b66b6f577ded0927247796d3cc30661286e556cf227077b16c`  
		Last Modified: Tue, 13 May 2025 23:56:18 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:3ea6c6c3c964ee4317d666960533c69ba5cfeae335191176e095d73c18617884
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
$ docker pull varnish@sha256:73855af0323500aec818851ac2775adb2075ba012849c6d9f7ae66a80a81871a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127755715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2416a3a733e0bcd8451f19dff388d0cf9639b7a4fb0405d453daf809ecf43c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a63fe15aa985166e0a536f16733c5108a400d7924f2d9e255c0fdc17483a7`  
		Last Modified: Tue, 01 Jul 2025 06:19:57 GMT  
		Size: 99.5 MB (99524819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f00144706708502c6ca62fad1808cc616a78de1f4fee6e717a406381d00957`  
		Last Modified: Tue, 01 Jul 2025 02:34:22 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:5fe26432899d928277277e73b7950a70acd3008bf3679cc61513798ad42d7d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93affad24d278f4006952a303dfaa72e03bf29ce2e335139a6661f6ed9ecf750`

```dockerfile
```

-	Layers:
	-	`sha256:d32a6c4b5e8d88ea5c052d0f6dbebca10055a0490091fe0dcf217eb5d131d823`  
		Last Modified: Tue, 01 Jul 2025 06:19:27 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d546048bdf9decdf83ff35b85c945c64424a2c45454947f90e642cfc3503c073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98278623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de534e855e7d7aff6838fdb59ef7d40f758aed1d6d6d9e1c9194a48aba036241`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e24917cd891f9d5ae1d2777c107e05262678dd8b4cbdd155454847751efae4`  
		Last Modified: Tue, 01 Jul 2025 08:57:10 GMT  
		Size: 74.3 MB (74339125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b947dec08812c0653ee92051ea8ac2e8a3e851428ec0b13da4ff64b47d3b86e`  
		Last Modified: Tue, 01 Jul 2025 08:57:01 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:17b3007883e565a862da70e5b58f360a7ccf12731ba26eb254091a966be4c966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8a889fd3b0a818870d5f6669753d69c950d72bced7b1b0ee53f592ac361bb1`

```dockerfile
```

-	Layers:
	-	`sha256:3e015e699a18830fefef9cdec2e6f3b8e74b9bc67f3e21b9919338e5fc8981f9`  
		Last Modified: Tue, 01 Jul 2025 09:19:20 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:9669977c18b26fee22609b5c01222f19c027762ce8d7bdbd19c122f7e4cbc58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122404230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc62f49c5f4a4609748464d3a197cab21c8b8c2858a5e419a0ffed4b93720656`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52493f864a7ea7e76396f86bdf9e9c7e549171ff77a71cc23926691410bd561d`  
		Last Modified: Tue, 01 Jul 2025 15:19:43 GMT  
		Size: 94.3 MB (94325799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219e0aa2e5e7f385c96000801923cb3ec29cc5e47755b610005295fb6d077b1d`  
		Last Modified: Tue, 01 Jul 2025 12:14:45 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:c244423326a51af935c87864c7662e4903d6f738ed0ff99503c4f985851314dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f3b8017bafae358fd913f470c57ae60a37452959455e7f92eb01f5cb281fa`

```dockerfile
```

-	Layers:
	-	`sha256:2e7bd3c8f173db3ad14d9576ca96736e9ca15c4a16d8e74df52832027cf6463c`  
		Last Modified: Tue, 01 Jul 2025 15:19:22 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:7a0cc82a8bf6f5bca7dd9d5b79271b3bead03d38e17de37a4d135885ca54e467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124893906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f392d5f8c15e9fcb5e91503f65e76a8f91ec8f76f1a430c6b0553c68c3d57d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28ce7101062bec3cdcc280044719a4889e578d9ea7e99a2c8cb2d0a7501eae3`  
		Last Modified: Tue, 01 Jul 2025 02:25:47 GMT  
		Size: 95.7 MB (95680721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1020eeb9c3c3d4471c4f899f48a869545850ee1e6547e0ddb6fe6214e8b4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:c4d9adf6edc38a0e245fc98f12ccd3c0626821dd32664f93e4435d62e0d019d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd59d9b7ccc734ca895ead671fc640c07c4a91e57fb6c7610d30dcd61c3acdfe`

```dockerfile
```

-	Layers:
	-	`sha256:e278cb2e177cb76411294b2dca5e98bdf483723d9b1e47cba336321c581a45db`  
		Last Modified: Tue, 01 Jul 2025 06:19:38 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:12204804569c23f22cb919eeed20c6883c18abd2efa8b9e744600206fc2dd663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130424352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1a0f619b1a1cf8acac4b47a7c814d4b3b145b7bdc25d326ece1f645f32faa3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac448ec4ef6903243dd1113c4e835f8d6f94cf17ad1b7d098b60707fbe32ecff`  
		Last Modified: Tue, 01 Jul 2025 05:06:11 GMT  
		Size: 98.4 MB (98350777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24314fab222fef3f118c833876e2127208d2f66124d4d7ebb223e8ba890133c9`  
		Last Modified: Tue, 01 Jul 2025 05:06:05 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:13fe9ba79150b6df03dc2d839c7c31c96b9e6868cfeeef8a78b8cb06a86f0886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca147d055c4478a8c7e8aefd7063c243299125c951337eccc617a5ec76eb1b9a`

```dockerfile
```

-	Layers:
	-	`sha256:84730cad3bf1309e99d4cfcb85d846836681307eb9edd8b2f1258942d89d12bc`  
		Last Modified: Tue, 01 Jul 2025 06:19:41 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:9a4914672be907c1e84b32253dcb1534a3bc90ab9f91616acebd03858468e434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105638217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f4051bd3877ddaa96f1f5b121fbb0794e82fc712a0a92df06e42675e40766`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 13 May 2025 22:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5e3acfd55d7be70f0cb0ec35643feeab794059804fb0394878dda0a1efc079`  
		Last Modified: Tue, 01 Jul 2025 05:30:02 GMT  
		Size: 78.7 MB (78749651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c1387deb44c299443963d18f577bc4de2ac7fefa0cff3a3f9a7db0b4caac8`  
		Last Modified: Tue, 01 Jul 2025 05:29:57 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:f8370a2dc1663f730cc441d92918dd3e2b7fc3c18582a8e10b3e15aef66008ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c955f5c7a388140da8ecf7fd602133bfcd73fbe8a95337476358129b7adc9642`

```dockerfile
```

-	Layers:
	-	`sha256:4d0b37496975156f5b4be420ebe283b80fa298514487e5d05921f6fc7a6744a9`  
		Last Modified: Tue, 01 Jul 2025 06:19:44 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json
