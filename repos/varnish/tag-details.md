<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.16`](#varnish6016)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.3`](#varnish773)
-	[`varnish:7.7.3-alpine`](#varnish773-alpine)
-	[`varnish:8`](#varnish8)
-	[`varnish:8-alpine`](#varnish8-alpine)
-	[`varnish:8.0`](#varnish80)
-	[`varnish:8.0-alpine`](#varnish80-alpine)
-	[`varnish:8.0.0`](#varnish800)
-	[`varnish:8.0.0-alpine`](#varnish800-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:855d6c2d3b99ab239649829f016c29217dc4fcb7e0372a2555e236036eae5195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:b0bb5130c045e4ed88893eeafbf6d8b1197d781605ae4f63a133c222bc95c838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c35d1f27f7233f4fa8eb5363593054e9aebb08d4e0587cac875afbaed15269`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:38:30 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:38:30 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:38:30 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:30 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055a1df36dfed0fadbdc059ee421ee1ad6c7bf9251a1b2cc008471f8cfdf2654`  
		Last Modified: Mon, 16 Mar 2026 22:38:43 GMT  
		Size: 75.3 MB (75320945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee086c1915b7ed773532f3663341b2516d4cd1536daa434e814d08de2e61e7d`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:9c96c92c25e84a14aa7c692bb557dd5f8809232fbd53b8e6490dc84b297becda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bdea2d2df2acb0efb583d102c2397b99556c9e7d0a3fd4205afc84c506430f`

```dockerfile
```

-	Layers:
	-	`sha256:00c2684bd4a8ab21306e221c438454b5d1290401d35d44f5654616b77c61fc3e`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 12.7 KB (12657 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0e0dd63b700b869e0d8fe8394a36082bbd43d587b1057f6d51e8397177a2bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e62fbb2a951812f6565857d87cbac71a2ba90d6d6efb99f5a486edd6caab06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:40:36 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:40:36 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:40:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:40:36 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:40:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:40:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:40:36 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9d9907a53af5e00389e3eea54067d788145e7262bfa2582c47732b88600d50`  
		Last Modified: Mon, 16 Mar 2026 22:40:48 GMT  
		Size: 70.3 MB (70299576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6364eaea38f3f8be3bdb617f0a30b07b010d54213da9dff418bb7bd58f61215f`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:76c67dc1e6b208fa6137cd91e0bd7a9d5913f85f5be2de3c148b277635b8479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6531325a26c3ec3b38e2b802d80ce7b5ab97311749cb9fbb84a6c535e984dd`

```dockerfile
```

-	Layers:
	-	`sha256:1ff656a98056e74c66c6382c20a86fa0b66bd4cddb489c765be5e878aa2c4f9a`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.16`

```console
$ docker pull varnish@sha256:855d6c2d3b99ab239649829f016c29217dc4fcb7e0372a2555e236036eae5195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.16` - linux; amd64

```console
$ docker pull varnish@sha256:b0bb5130c045e4ed88893eeafbf6d8b1197d781605ae4f63a133c222bc95c838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c35d1f27f7233f4fa8eb5363593054e9aebb08d4e0587cac875afbaed15269`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:38:30 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:38:30 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:38:30 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:30 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055a1df36dfed0fadbdc059ee421ee1ad6c7bf9251a1b2cc008471f8cfdf2654`  
		Last Modified: Mon, 16 Mar 2026 22:38:43 GMT  
		Size: 75.3 MB (75320945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee086c1915b7ed773532f3663341b2516d4cd1536daa434e814d08de2e61e7d`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:9c96c92c25e84a14aa7c692bb557dd5f8809232fbd53b8e6490dc84b297becda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bdea2d2df2acb0efb583d102c2397b99556c9e7d0a3fd4205afc84c506430f`

```dockerfile
```

-	Layers:
	-	`sha256:00c2684bd4a8ab21306e221c438454b5d1290401d35d44f5654616b77c61fc3e`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 12.7 KB (12657 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0e0dd63b700b869e0d8fe8394a36082bbd43d587b1057f6d51e8397177a2bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e62fbb2a951812f6565857d87cbac71a2ba90d6d6efb99f5a486edd6caab06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:40:36 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:40:36 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:40:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:40:36 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:40:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:40:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:40:36 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9d9907a53af5e00389e3eea54067d788145e7262bfa2582c47732b88600d50`  
		Last Modified: Mon, 16 Mar 2026 22:40:48 GMT  
		Size: 70.3 MB (70299576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6364eaea38f3f8be3bdb617f0a30b07b010d54213da9dff418bb7bd58f61215f`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:76c67dc1e6b208fa6137cd91e0bd7a9d5913f85f5be2de3c148b277635b8479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6531325a26c3ec3b38e2b802d80ce7b5ab97311749cb9fbb84a6c535e984dd`

```dockerfile
```

-	Layers:
	-	`sha256:1ff656a98056e74c66c6382c20a86fa0b66bd4cddb489c765be5e878aa2c4f9a`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:3f3df388d03695f4ff1efe75cc69a4311d8c5d44411cd99d2f0707056b056f29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7` - linux; amd64

```console
$ docker pull varnish@sha256:cc9fc0948d1e2881579e9d255b3b2d9e4ad2118945051919a3e8244ed2a26a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116342605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3d8d85742067991aaf2285adb0f6d2a3ed1bedb3ac02be1397c06d728dec93`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:52 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_VERSION=7.7.3
# Mon, 16 Mar 2026 22:38:52 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 16 Mar 2026 22:38:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:38:52 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:52 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:52 GMT
USER varnish
# Mon, 16 Mar 2026 22:38:52 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c400eedd0902bb584b83ea0f4e7863e586754b85ba73b5a7966f4913841f970a`  
		Last Modified: Mon, 16 Mar 2026 22:39:06 GMT  
		Size: 86.6 MB (86565060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9acfc49ddb1c683cb77464bb6df4858370f041db2bf7ff6b2b9b5276ef79b4c`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:afd2ec1065ea4bbec9ea3e8928d67ced40390ff12cab6ad658208bfd010bbf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bc83c9e7322dcf54d4c0fd76ed164c48a10ab67e0a9c10071763f18d0b07ae`

```dockerfile
```

-	Layers:
	-	`sha256:9bfc471f4bb6d52e3beda5c709a7c3d6ca95d4bf6e63a6fc4a2ca94448fad000`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 19.1 KB (19053 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:eb2dcfd18eecd8bb432ee638208febb7e543bccadd015a42c9aa3aef9bf93b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ba07e2d11f7f9b7167fe68cb954cdbe0d480c88a211beea2302ed187d4fcfa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:41:03 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_VERSION=7.7.3
# Mon, 16 Mar 2026 22:41:03 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 16 Mar 2026 22:41:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:41:03 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:41:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:41:04 GMT
USER varnish
# Mon, 16 Mar 2026 22:41:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:41:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8c6c154a2922669f3d6dbb2a3a4518044937f236a5fb7800f03dba7e0f9c`  
		Last Modified: Mon, 16 Mar 2026 22:41:16 GMT  
		Size: 80.4 MB (80386683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04be858a36c74e1fd30f5f5519194ab7d3d844c39cddae8c0c09ab114421444`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f2c257eeb9a97ad026331c8fa27beced5a55dc9b96f40e6ff60320d457202f`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:948750a30e04e827c3e3a4ccfa4a69e3bdabc2247894f684fb7b3aea48eb9492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb79094ebdb52f2aa1cdcc1aa7c2a5a0e3e4b1e0be7a075271fde9240be1135d`

```dockerfile
```

-	Layers:
	-	`sha256:7d0b8f0602fa0ab8a784ba5b79e397c7bd6caac24f34699fe620a32d5e1c43e5`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:95deada23d0ef0cd1005cfe32463f3390f31a63f13682996bccdb5b01ea7f291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:8aa05c32b87720c21201f23664c14e58218e6a8bf2d240192d61ddf7cbda1543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b3a4a43c039fde71b875c7d203b302d8f539cf7d6ea66bd68203662cfd84c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:08 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:08 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:08 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:08 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a04f2c14282af7f7e529680683c4281801fe0d25060b1f1849b5b10ce75207`  
		Last Modified: Wed, 28 Jan 2026 02:40:21 GMT  
		Size: 76.7 MB (76742117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ff28a6f82e4f8ababee51c3cba66677a5d436c027f202cff74cdfaa22b2fa`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e3640c70635b2fb032b6853f07c74fea52315c1157b90d728b171a25b855a6`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fdbfb5b2598b29dc6fcc4576ff7054763636eb08b994d768f3b662e46af7cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70f4eca00c39ae1979c06ee1adef5eba46dbea1c6b4bb8dddc0c9da233cf6a7`

```dockerfile
```

-	Layers:
	-	`sha256:af700eba3659b121f6e7f4f91bec07eb72c5b17f00d6e85559d34eae8c6939a5`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e08f69115921e2084edfdc49c70244ca6e2c2830f7cd882ce3fc68302320e795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77534209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68875f332b81c8a9f0b8157adf6aca453c9ce66478997f3899c83048bee86613`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:14 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:14 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:14 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:14 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:14 GMT
CMD []
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf710ef050705257a3b1ccc4556cc95fed48da6153f9dee22ff258bd3f4a2704`  
		Last Modified: Wed, 28 Jan 2026 02:40:27 GMT  
		Size: 73.4 MB (73392634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c78500b776f154686015e0536a78e6cbcf306c95ed7a6dab1769067fbaa5`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086e9e0255e2a3935f436f74da42da55a0fa0de25ce1aaee7c10dfba1a1882b`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b3342940e958392acaafe6dc63153ff912a0c9ef8b4d773520b8d0e57c4f8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64f6ef49b079355c29686ebba4c3599233207673cca81322e56af6cf83e9fb`

```dockerfile
```

-	Layers:
	-	`sha256:14078e9f50c83d2b5b9d2201394b09e185e22d9f12db3c8385b168e27f1b5679`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3`

```console
$ docker pull varnish@sha256:3f3df388d03695f4ff1efe75cc69a4311d8c5d44411cd99d2f0707056b056f29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7.3` - linux; amd64

```console
$ docker pull varnish@sha256:cc9fc0948d1e2881579e9d255b3b2d9e4ad2118945051919a3e8244ed2a26a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116342605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3d8d85742067991aaf2285adb0f6d2a3ed1bedb3ac02be1397c06d728dec93`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:52 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_VERSION=7.7.3
# Mon, 16 Mar 2026 22:38:52 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 16 Mar 2026 22:38:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:38:52 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:52 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:52 GMT
USER varnish
# Mon, 16 Mar 2026 22:38:52 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c400eedd0902bb584b83ea0f4e7863e586754b85ba73b5a7966f4913841f970a`  
		Last Modified: Mon, 16 Mar 2026 22:39:06 GMT  
		Size: 86.6 MB (86565060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9acfc49ddb1c683cb77464bb6df4858370f041db2bf7ff6b2b9b5276ef79b4c`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:afd2ec1065ea4bbec9ea3e8928d67ced40390ff12cab6ad658208bfd010bbf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bc83c9e7322dcf54d4c0fd76ed164c48a10ab67e0a9c10071763f18d0b07ae`

```dockerfile
```

-	Layers:
	-	`sha256:9bfc471f4bb6d52e3beda5c709a7c3d6ca95d4bf6e63a6fc4a2ca94448fad000`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 19.1 KB (19053 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:eb2dcfd18eecd8bb432ee638208febb7e543bccadd015a42c9aa3aef9bf93b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ba07e2d11f7f9b7167fe68cb954cdbe0d480c88a211beea2302ed187d4fcfa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:41:03 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_VERSION=7.7.3
# Mon, 16 Mar 2026 22:41:03 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 16 Mar 2026 22:41:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:41:03 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:41:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:41:04 GMT
USER varnish
# Mon, 16 Mar 2026 22:41:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:41:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8c6c154a2922669f3d6dbb2a3a4518044937f236a5fb7800f03dba7e0f9c`  
		Last Modified: Mon, 16 Mar 2026 22:41:16 GMT  
		Size: 80.4 MB (80386683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04be858a36c74e1fd30f5f5519194ab7d3d844c39cddae8c0c09ab114421444`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f2c257eeb9a97ad026331c8fa27beced5a55dc9b96f40e6ff60320d457202f`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:948750a30e04e827c3e3a4ccfa4a69e3bdabc2247894f684fb7b3aea48eb9492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb79094ebdb52f2aa1cdcc1aa7c2a5a0e3e4b1e0be7a075271fde9240be1135d`

```dockerfile
```

-	Layers:
	-	`sha256:7d0b8f0602fa0ab8a784ba5b79e397c7bd6caac24f34699fe620a32d5e1c43e5`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3-alpine`

```console
$ docker pull varnish@sha256:95deada23d0ef0cd1005cfe32463f3390f31a63f13682996bccdb5b01ea7f291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:8aa05c32b87720c21201f23664c14e58218e6a8bf2d240192d61ddf7cbda1543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b3a4a43c039fde71b875c7d203b302d8f539cf7d6ea66bd68203662cfd84c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:08 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:08 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:08 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:08 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a04f2c14282af7f7e529680683c4281801fe0d25060b1f1849b5b10ce75207`  
		Last Modified: Wed, 28 Jan 2026 02:40:21 GMT  
		Size: 76.7 MB (76742117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ff28a6f82e4f8ababee51c3cba66677a5d436c027f202cff74cdfaa22b2fa`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e3640c70635b2fb032b6853f07c74fea52315c1157b90d728b171a25b855a6`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fdbfb5b2598b29dc6fcc4576ff7054763636eb08b994d768f3b662e46af7cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70f4eca00c39ae1979c06ee1adef5eba46dbea1c6b4bb8dddc0c9da233cf6a7`

```dockerfile
```

-	Layers:
	-	`sha256:af700eba3659b121f6e7f4f91bec07eb72c5b17f00d6e85559d34eae8c6939a5`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e08f69115921e2084edfdc49c70244ca6e2c2830f7cd882ce3fc68302320e795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77534209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68875f332b81c8a9f0b8157adf6aca453c9ce66478997f3899c83048bee86613`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:14 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:14 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:14 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:14 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:14 GMT
CMD []
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf710ef050705257a3b1ccc4556cc95fed48da6153f9dee22ff258bd3f4a2704`  
		Last Modified: Wed, 28 Jan 2026 02:40:27 GMT  
		Size: 73.4 MB (73392634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c78500b776f154686015e0536a78e6cbcf306c95ed7a6dab1769067fbaa5`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086e9e0255e2a3935f436f74da42da55a0fa0de25ce1aaee7c10dfba1a1882b`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b3342940e958392acaafe6dc63153ff912a0c9ef8b4d773520b8d0e57c4f8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64f6ef49b079355c29686ebba4c3599233207673cca81322e56af6cf83e9fb`

```dockerfile
```

-	Layers:
	-	`sha256:14078e9f50c83d2b5b9d2201394b09e185e22d9f12db3c8385b168e27f1b5679`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:6d0d6d4e01730930a3ed5f7de02dfb5963b620087a3ab2a2024d9786ccb2a452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:02c47c89db40c8b93c73d13830e0a2c9aa8796837d33aa3eb31b65579c62503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121961188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81011423be26eeece042fee45a1122a0647c8508d13c36b1561a5a8dc15bf88e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:37:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:37:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:37:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:37:40 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:37:40 GMT
USER varnish
# Mon, 16 Mar 2026 22:37:40 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:37:40 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5574fad1be0f624140ff6b6c0d1c0b07ad564f5fa83bd2d3c6585cbe7d96f22`  
		Last Modified: Mon, 16 Mar 2026 22:37:53 GMT  
		Size: 92.2 MB (92182565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfec074bab00bd03f91ba3ff33d514773c320274d80ffd237244b8c188a87237`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd70f70a772a74a3fab80b7e8ee24cf71c150aa12f60fe4f6b56d573dbb472d1`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:6f6dce6c396aa6eda9d3c0c83a036d91f7b5e3c383d8e4cf7f072c9bd3181c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0420e8d7461ac6a226e39eac768888a2172515e185c034a67b1f13e5979a96d`

```dockerfile
```

-	Layers:
	-	`sha256:d327d031f82eda576a70be76fdc5ae09d2b4abf1578c7e4f09dbf8b8addc113e`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 20.9 KB (20877 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:41cce21a6cdba8bbfa570169f1c5f0bd4cc49687136c4a82d1d8787345a2a6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115940963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff01a91dec15031d07578459775db341bf01a13badeb8e2f03a9e3060e17bd3c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:39:59 GMT
USER varnish
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4164d93eacca773496c858b30ece8dc13b5a0594922e9bdd78bc3305b752da`  
		Last Modified: Mon, 16 Mar 2026 22:40:13 GMT  
		Size: 85.8 MB (85799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae9d1ef0dee6f09565d29d8752e8a6c99fcb686f7cbc4e510363ecbdc5fbb73`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7761b9b9ea98bbf83196fc50b1fed5105b9a1155977ccc31e387b9beb3bc375`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67a11b37d9f8a8f2efed608490cad970c1bddc9b1b32fcec40284ab418adb5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:b63fe66a633f6bd58b000dc9967793cf8bee878c96f10d04c15d67d56346082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc51bb523e6a6fe4717568819003d3c8d6282c88b329648cf049dbf9bd06df5`

```dockerfile
```

-	Layers:
	-	`sha256:bad38f5f46d18c20c254bdd8125356eab0b81d303bea36a4aea58a6dc29c1c67`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0`

```console
$ docker pull varnish@sha256:6d0d6d4e01730930a3ed5f7de02dfb5963b620087a3ab2a2024d9786ccb2a452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:02c47c89db40c8b93c73d13830e0a2c9aa8796837d33aa3eb31b65579c62503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121961188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81011423be26eeece042fee45a1122a0647c8508d13c36b1561a5a8dc15bf88e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:37:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:37:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:37:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:37:40 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:37:40 GMT
USER varnish
# Mon, 16 Mar 2026 22:37:40 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:37:40 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5574fad1be0f624140ff6b6c0d1c0b07ad564f5fa83bd2d3c6585cbe7d96f22`  
		Last Modified: Mon, 16 Mar 2026 22:37:53 GMT  
		Size: 92.2 MB (92182565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfec074bab00bd03f91ba3ff33d514773c320274d80ffd237244b8c188a87237`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd70f70a772a74a3fab80b7e8ee24cf71c150aa12f60fe4f6b56d573dbb472d1`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:6f6dce6c396aa6eda9d3c0c83a036d91f7b5e3c383d8e4cf7f072c9bd3181c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0420e8d7461ac6a226e39eac768888a2172515e185c034a67b1f13e5979a96d`

```dockerfile
```

-	Layers:
	-	`sha256:d327d031f82eda576a70be76fdc5ae09d2b4abf1578c7e4f09dbf8b8addc113e`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 20.9 KB (20877 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:41cce21a6cdba8bbfa570169f1c5f0bd4cc49687136c4a82d1d8787345a2a6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115940963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff01a91dec15031d07578459775db341bf01a13badeb8e2f03a9e3060e17bd3c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:39:59 GMT
USER varnish
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4164d93eacca773496c858b30ece8dc13b5a0594922e9bdd78bc3305b752da`  
		Last Modified: Mon, 16 Mar 2026 22:40:13 GMT  
		Size: 85.8 MB (85799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae9d1ef0dee6f09565d29d8752e8a6c99fcb686f7cbc4e510363ecbdc5fbb73`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7761b9b9ea98bbf83196fc50b1fed5105b9a1155977ccc31e387b9beb3bc375`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67a11b37d9f8a8f2efed608490cad970c1bddc9b1b32fcec40284ab418adb5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b63fe66a633f6bd58b000dc9967793cf8bee878c96f10d04c15d67d56346082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc51bb523e6a6fe4717568819003d3c8d6282c88b329648cf049dbf9bd06df5`

```dockerfile
```

-	Layers:
	-	`sha256:bad38f5f46d18c20c254bdd8125356eab0b81d303bea36a4aea58a6dc29c1c67`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.0`

```console
$ docker pull varnish@sha256:6d0d6d4e01730930a3ed5f7de02dfb5963b620087a3ab2a2024d9786ccb2a452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.0` - linux; amd64

```console
$ docker pull varnish@sha256:02c47c89db40c8b93c73d13830e0a2c9aa8796837d33aa3eb31b65579c62503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121961188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81011423be26eeece042fee45a1122a0647c8508d13c36b1561a5a8dc15bf88e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:37:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:37:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:37:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:37:40 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:37:40 GMT
USER varnish
# Mon, 16 Mar 2026 22:37:40 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:37:40 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5574fad1be0f624140ff6b6c0d1c0b07ad564f5fa83bd2d3c6585cbe7d96f22`  
		Last Modified: Mon, 16 Mar 2026 22:37:53 GMT  
		Size: 92.2 MB (92182565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfec074bab00bd03f91ba3ff33d514773c320274d80ffd237244b8c188a87237`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd70f70a772a74a3fab80b7e8ee24cf71c150aa12f60fe4f6b56d573dbb472d1`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:6f6dce6c396aa6eda9d3c0c83a036d91f7b5e3c383d8e4cf7f072c9bd3181c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0420e8d7461ac6a226e39eac768888a2172515e185c034a67b1f13e5979a96d`

```dockerfile
```

-	Layers:
	-	`sha256:d327d031f82eda576a70be76fdc5ae09d2b4abf1578c7e4f09dbf8b8addc113e`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 20.9 KB (20877 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:41cce21a6cdba8bbfa570169f1c5f0bd4cc49687136c4a82d1d8787345a2a6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115940963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff01a91dec15031d07578459775db341bf01a13badeb8e2f03a9e3060e17bd3c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:39:59 GMT
USER varnish
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4164d93eacca773496c858b30ece8dc13b5a0594922e9bdd78bc3305b752da`  
		Last Modified: Mon, 16 Mar 2026 22:40:13 GMT  
		Size: 85.8 MB (85799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae9d1ef0dee6f09565d29d8752e8a6c99fcb686f7cbc4e510363ecbdc5fbb73`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7761b9b9ea98bbf83196fc50b1fed5105b9a1155977ccc31e387b9beb3bc375`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67a11b37d9f8a8f2efed608490cad970c1bddc9b1b32fcec40284ab418adb5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b63fe66a633f6bd58b000dc9967793cf8bee878c96f10d04c15d67d56346082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc51bb523e6a6fe4717568819003d3c8d6282c88b329648cf049dbf9bd06df5`

```dockerfile
```

-	Layers:
	-	`sha256:bad38f5f46d18c20c254bdd8125356eab0b81d303bea36a4aea58a6dc29c1c67`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.0-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:6d0d6d4e01730930a3ed5f7de02dfb5963b620087a3ab2a2024d9786ccb2a452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:02c47c89db40c8b93c73d13830e0a2c9aa8796837d33aa3eb31b65579c62503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121961188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81011423be26eeece042fee45a1122a0647c8508d13c36b1561a5a8dc15bf88e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:37:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:37:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:37:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:37:40 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:37:40 GMT
USER varnish
# Mon, 16 Mar 2026 22:37:40 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:37:40 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5574fad1be0f624140ff6b6c0d1c0b07ad564f5fa83bd2d3c6585cbe7d96f22`  
		Last Modified: Mon, 16 Mar 2026 22:37:53 GMT  
		Size: 92.2 MB (92182565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfec074bab00bd03f91ba3ff33d514773c320274d80ffd237244b8c188a87237`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd70f70a772a74a3fab80b7e8ee24cf71c150aa12f60fe4f6b56d573dbb472d1`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:6f6dce6c396aa6eda9d3c0c83a036d91f7b5e3c383d8e4cf7f072c9bd3181c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0420e8d7461ac6a226e39eac768888a2172515e185c034a67b1f13e5979a96d`

```dockerfile
```

-	Layers:
	-	`sha256:d327d031f82eda576a70be76fdc5ae09d2b4abf1578c7e4f09dbf8b8addc113e`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 20.9 KB (20877 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:41cce21a6cdba8bbfa570169f1c5f0bd4cc49687136c4a82d1d8787345a2a6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115940963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff01a91dec15031d07578459775db341bf01a13badeb8e2f03a9e3060e17bd3c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:39:59 GMT
USER varnish
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4164d93eacca773496c858b30ece8dc13b5a0594922e9bdd78bc3305b752da`  
		Last Modified: Mon, 16 Mar 2026 22:40:13 GMT  
		Size: 85.8 MB (85799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae9d1ef0dee6f09565d29d8752e8a6c99fcb686f7cbc4e510363ecbdc5fbb73`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7761b9b9ea98bbf83196fc50b1fed5105b9a1155977ccc31e387b9beb3bc375`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67a11b37d9f8a8f2efed608490cad970c1bddc9b1b32fcec40284ab418adb5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b63fe66a633f6bd58b000dc9967793cf8bee878c96f10d04c15d67d56346082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc51bb523e6a6fe4717568819003d3c8d6282c88b329648cf049dbf9bd06df5`

```dockerfile
```

-	Layers:
	-	`sha256:bad38f5f46d18c20c254bdd8125356eab0b81d303bea36a4aea58a6dc29c1c67`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:a84e1d4adb58b1f0594efbc95b9854c37040aafbbb990fa4889d6520a2feea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:313c1e39011cd7ad60a797012574cf43ec9b3f652368766eb8f658134c798e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91772446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db2dd9ec648dcf29eb5e73fb988e6337591e92a9cd3dc40566579e5dfc69a0b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:32:53 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:32:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:32:53 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:32:53 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:32:53 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:32:53 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:32:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:32:53 GMT
USER varnish
# Wed, 28 Jan 2026 18:32:53 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:32:53 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023c28f50298fde5fdebfb9183a14c01add9e56dbd5e465fbb5f20091e66b26`  
		Last Modified: Wed, 28 Jan 2026 18:33:06 GMT  
		Size: 87.9 MB (87907492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ab80124716fd6fd1dea26c10cb19d9956f00e9310f54b211bedf51903d0a8`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed37e8718e0c2f976041d5825a05251d01a2cccd7ea651e4faba3892a74a3c7`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3e6fd73e1c2d4af26c7e5621e4317be18bcfc94308e5b6beb6a72cd170854`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f5a6df222303ec11afdd7aba8e6ce117da6dca249c39fcb4c7bf80666ffa4e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e35f19446543c684a63b0d3e4df83aadc77b84dbd5ba27017204e16548e5cf`

```dockerfile
```

-	Layers:
	-	`sha256:2472b92b11950f0ccd3dac0294bf9c31e2174882ccbec33de210089fab5ec428`  
		Last Modified: Wed, 28 Jan 2026 18:33:04 GMT  
		Size: 20.7 KB (20687 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5012ddbf256e65054b99e3f27bae23f4973c3427d3e69882536053454ae033dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83538388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6858c7d69f1ef19e0c93fe2588a96b69e65e9c3918e563a55fbb19e09a0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 18:45:55 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_VERSION=8.0.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 28 Jan 2026 18:45:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 28 Jan 2026 18:45:55 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 18:45:55 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 18:45:55 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 18:45:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 18:45:55 GMT
USER varnish
# Wed, 28 Jan 2026 18:45:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 18:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24d757c3e5486bd934e3ed2ab115041c3cd5eeca9bf88d5e0fe5e73f1c01bd`  
		Last Modified: Wed, 28 Jan 2026 18:46:07 GMT  
		Size: 79.3 MB (79338167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a29fb6864bfa14adb7c64c7cd4a92ae6740e89da8dc5544e4032c5670f7d1`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca8d9ee0017ec696497e5afaafe59a065eb02feac3a273c07d5ec27b56fd34`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ce2d813532284a2265d0ea39dfcbd5a65dc2b4b6c09af121ab8edd31c46b`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cb09b7c875b608f6488d947d4fae3713abeb40a55f44b7ce5e011b5bdfb77cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c3dbcb1e49cbee0a8f8b985cb8f495cd814543ff07752a680cb0d5cb573948`

```dockerfile
```

-	Layers:
	-	`sha256:7b786c97ea1f2e5b349e6674dcdbee3e869393e0ba482f7be67c9bab7fd4be22`  
		Last Modified: Wed, 28 Jan 2026 18:46:05 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:6d0d6d4e01730930a3ed5f7de02dfb5963b620087a3ab2a2024d9786ccb2a452
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:02c47c89db40c8b93c73d13830e0a2c9aa8796837d33aa3eb31b65579c62503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121961188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81011423be26eeece042fee45a1122a0647c8508d13c36b1561a5a8dc15bf88e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:37:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:37:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:37:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:37:39 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:37:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:37:40 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:37:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:37:40 GMT
USER varnish
# Mon, 16 Mar 2026 22:37:40 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:37:40 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5574fad1be0f624140ff6b6c0d1c0b07ad564f5fa83bd2d3c6585cbe7d96f22`  
		Last Modified: Mon, 16 Mar 2026 22:37:53 GMT  
		Size: 92.2 MB (92182565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfec074bab00bd03f91ba3ff33d514773c320274d80ffd237244b8c188a87237`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd70f70a772a74a3fab80b7e8ee24cf71c150aa12f60fe4f6b56d573dbb472d1`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:6f6dce6c396aa6eda9d3c0c83a036d91f7b5e3c383d8e4cf7f072c9bd3181c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0420e8d7461ac6a226e39eac768888a2172515e185c034a67b1f13e5979a96d`

```dockerfile
```

-	Layers:
	-	`sha256:d327d031f82eda576a70be76fdc5ae09d2b4abf1578c7e4f09dbf8b8addc113e`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 20.9 KB (20877 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:41cce21a6cdba8bbfa570169f1c5f0bd4cc49687136c4a82d1d8787345a2a6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115940963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff01a91dec15031d07578459775db341bf01a13badeb8e2f03a9e3060e17bd3c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 16 Mar 2026 22:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 16 Mar 2026 22:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:39:59 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:39:59 GMT
USER varnish
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4164d93eacca773496c858b30ece8dc13b5a0594922e9bdd78bc3305b752da`  
		Last Modified: Mon, 16 Mar 2026 22:40:13 GMT  
		Size: 85.8 MB (85799433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae9d1ef0dee6f09565d29d8752e8a6c99fcb686f7cbc4e510363ecbdc5fbb73`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7761b9b9ea98bbf83196fc50b1fed5105b9a1155977ccc31e387b9beb3bc375`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67a11b37d9f8a8f2efed608490cad970c1bddc9b1b32fcec40284ab418adb5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:b63fe66a633f6bd58b000dc9967793cf8bee878c96f10d04c15d67d56346082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc51bb523e6a6fe4717568819003d3c8d6282c88b329648cf049dbf9bd06df5`

```dockerfile
```

-	Layers:
	-	`sha256:bad38f5f46d18c20c254bdd8125356eab0b81d303bea36a4aea58a6dc29c1c67`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:3f3df388d03695f4ff1efe75cc69a4311d8c5d44411cd99d2f0707056b056f29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:cc9fc0948d1e2881579e9d255b3b2d9e4ad2118945051919a3e8244ed2a26a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116342605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3d8d85742067991aaf2285adb0f6d2a3ed1bedb3ac02be1397c06d728dec93`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:52 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_VERSION=7.7.3
# Mon, 16 Mar 2026 22:38:52 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 16 Mar 2026 22:38:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 16 Mar 2026 22:38:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:52 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:38:52 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:52 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:52 GMT
USER varnish
# Mon, 16 Mar 2026 22:38:52 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c400eedd0902bb584b83ea0f4e7863e586754b85ba73b5a7966f4913841f970a`  
		Last Modified: Mon, 16 Mar 2026 22:39:06 GMT  
		Size: 86.6 MB (86565060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cee06732c1b87d2e740a861819b412c1493c1ab19d5854ff4cad38fae53ef`  
		Last Modified: Mon, 16 Mar 2026 22:37:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9acfc49ddb1c683cb77464bb6df4858370f041db2bf7ff6b2b9b5276ef79b4c`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:afd2ec1065ea4bbec9ea3e8928d67ced40390ff12cab6ad658208bfd010bbf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bc83c9e7322dcf54d4c0fd76ed164c48a10ab67e0a9c10071763f18d0b07ae`

```dockerfile
```

-	Layers:
	-	`sha256:9bfc471f4bb6d52e3beda5c709a7c3d6ca95d4bf6e63a6fc4a2ca94448fad000`  
		Last Modified: Mon, 16 Mar 2026 22:39:03 GMT  
		Size: 19.1 KB (19053 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:eb2dcfd18eecd8bb432ee638208febb7e543bccadd015a42c9aa3aef9bf93b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ba07e2d11f7f9b7167fe68cb954cdbe0d480c88a211beea2302ed187d4fcfa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:41:03 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_VERSION=7.7.3
# Mon, 16 Mar 2026 22:41:03 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 16 Mar 2026 22:41:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 16 Mar 2026 22:41:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:41:03 GMT
ENV VSM_NOPID=1
# Mon, 16 Mar 2026 22:41:03 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:41:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Mar 2026 22:41:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:41:04 GMT
USER varnish
# Mon, 16 Mar 2026 22:41:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:41:04 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8c6c154a2922669f3d6dbb2a3a4518044937f236a5fb7800f03dba7e0f9c`  
		Last Modified: Mon, 16 Mar 2026 22:41:16 GMT  
		Size: 80.4 MB (80386683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04be858a36c74e1fd30f5f5519194ab7d3d844c39cddae8c0c09ab114421444`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f2c257eeb9a97ad026331c8fa27beced5a55dc9b96f40e6ff60320d457202f`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:948750a30e04e827c3e3a4ccfa4a69e3bdabc2247894f684fb7b3aea48eb9492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb79094ebdb52f2aa1cdcc1aa7c2a5a0e3e4b1e0be7a075271fde9240be1135d`

```dockerfile
```

-	Layers:
	-	`sha256:7d0b8f0602fa0ab8a784ba5b79e397c7bd6caac24f34699fe620a32d5e1c43e5`  
		Last Modified: Mon, 16 Mar 2026 22:41:14 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:95deada23d0ef0cd1005cfe32463f3390f31a63f13682996bccdb5b01ea7f291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:8aa05c32b87720c21201f23664c14e58218e6a8bf2d240192d61ddf7cbda1543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b3a4a43c039fde71b875c7d203b302d8f539cf7d6ea66bd68203662cfd84c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:08 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:08 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:08 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:08 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:08 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:08 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:08 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:08 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a04f2c14282af7f7e529680683c4281801fe0d25060b1f1849b5b10ce75207`  
		Last Modified: Wed, 28 Jan 2026 02:40:21 GMT  
		Size: 76.7 MB (76742117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ff28a6f82e4f8ababee51c3cba66677a5d436c027f202cff74cdfaa22b2fa`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e3640c70635b2fb032b6853f07c74fea52315c1157b90d728b171a25b855a6`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:fdbfb5b2598b29dc6fcc4576ff7054763636eb08b994d768f3b662e46af7cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70f4eca00c39ae1979c06ee1adef5eba46dbea1c6b4bb8dddc0c9da233cf6a7`

```dockerfile
```

-	Layers:
	-	`sha256:af700eba3659b121f6e7f4f91bec07eb72c5b17f00d6e85559d34eae8c6939a5`  
		Last Modified: Wed, 28 Jan 2026 02:40:19 GMT  
		Size: 18.8 KB (18840 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e08f69115921e2084edfdc49c70244ca6e2c2830f7cd882ce3fc68302320e795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77534209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68875f332b81c8a9f0b8157adf6aca453c9ce66478997f3899c83048bee86613`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:14 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_VERSION=7.7.3
# Wed, 28 Jan 2026 02:40:14 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Wed, 28 Jan 2026 02:40:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Wed, 28 Jan 2026 02:40:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 28 Jan 2026 02:40:14 GMT
ENV VSM_NOPID=1
# Wed, 28 Jan 2026 02:40:14 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
WORKDIR /etc/varnish
# Wed, 28 Jan 2026 02:40:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 28 Jan 2026 02:40:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 28 Jan 2026 02:40:14 GMT
USER varnish
# Wed, 28 Jan 2026 02:40:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 28 Jan 2026 02:40:14 GMT
CMD []
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf710ef050705257a3b1ccc4556cc95fed48da6153f9dee22ff258bd3f4a2704`  
		Last Modified: Wed, 28 Jan 2026 02:40:27 GMT  
		Size: 73.4 MB (73392634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c78500b776f154686015e0536a78e6cbcf306c95ed7a6dab1769067fbaa5`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086e9e0255e2a3935f436f74da42da55a0fa0de25ce1aaee7c10dfba1a1882b`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:b3342940e958392acaafe6dc63153ff912a0c9ef8b4d773520b8d0e57c4f8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64f6ef49b079355c29686ebba4c3599233207673cca81322e56af6cf83e9fb`

```dockerfile
```

-	Layers:
	-	`sha256:14078e9f50c83d2b5b9d2201394b09e185e22d9f12db3c8385b168e27f1b5679`  
		Last Modified: Wed, 28 Jan 2026 02:40:25 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:855d6c2d3b99ab239649829f016c29217dc4fcb7e0372a2555e236036eae5195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:b0bb5130c045e4ed88893eeafbf6d8b1197d781605ae4f63a133c222bc95c838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c35d1f27f7233f4fa8eb5363593054e9aebb08d4e0587cac875afbaed15269`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:38:30 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:38:30 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:38:30 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:30 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055a1df36dfed0fadbdc059ee421ee1ad6c7bf9251a1b2cc008471f8cfdf2654`  
		Last Modified: Mon, 16 Mar 2026 22:38:43 GMT  
		Size: 75.3 MB (75320945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee086c1915b7ed773532f3663341b2516d4cd1536daa434e814d08de2e61e7d`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:9c96c92c25e84a14aa7c692bb557dd5f8809232fbd53b8e6490dc84b297becda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bdea2d2df2acb0efb583d102c2397b99556c9e7d0a3fd4205afc84c506430f`

```dockerfile
```

-	Layers:
	-	`sha256:00c2684bd4a8ab21306e221c438454b5d1290401d35d44f5654616b77c61fc3e`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 12.7 KB (12657 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0e0dd63b700b869e0d8fe8394a36082bbd43d587b1057f6d51e8397177a2bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e62fbb2a951812f6565857d87cbac71a2ba90d6d6efb99f5a486edd6caab06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:40:36 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:40:36 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:40:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:40:36 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:40:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:40:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:40:36 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9d9907a53af5e00389e3eea54067d788145e7262bfa2582c47732b88600d50`  
		Last Modified: Mon, 16 Mar 2026 22:40:48 GMT  
		Size: 70.3 MB (70299576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6364eaea38f3f8be3bdb617f0a30b07b010d54213da9dff418bb7bd58f61215f`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:76c67dc1e6b208fa6137cd91e0bd7a9d5913f85f5be2de3c148b277635b8479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6531325a26c3ec3b38e2b802d80ce7b5ab97311749cb9fbb84a6c535e984dd`

```dockerfile
```

-	Layers:
	-	`sha256:1ff656a98056e74c66c6382c20a86fa0b66bd4cddb489c765be5e878aa2c4f9a`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json
