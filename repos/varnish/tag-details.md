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
$ docker pull varnish@sha256:b61dde4047098837f0b22b0855e57ce01797471f586e377cd559197c50627412
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:550aac2613064f8ae7e2355c72b60120ed40dfe110b65fa2ab70c4b0eb221579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4d432dcec47aa9b3913e33012f8bfde2d364e2c04a752509be48349185e06d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:07 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 24 Feb 2026 19:20:07 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 24 Feb 2026 19:20:07 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 24 Feb 2026 19:20:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:20:07 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 24 Feb 2026 19:20:07 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:20:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:20:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:20:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:20:07 GMT
CMD []
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5270969c016ab948ef843d0dafc3c5da8d1fb773ecdb3b6e1501b1861f1201a`  
		Last Modified: Tue, 24 Feb 2026 19:20:19 GMT  
		Size: 75.3 MB (75320899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed68ad79d2d4bcf843f875ee25a8f4997444cf992e8efb948fa9c61fca5b66`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:3b87f58b049ceae137f9e6c0ccd8288ba475fb634bc454689b939886c2938a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502c1825474e56e1445ffe978ab749d5025dcad4e05373a6322e35cb83980c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f9ec876009f49e3cb189387a17dc50137918fc09afc295f466f03ae4a3bac3ec`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 12.7 KB (12655 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1de539549e9d9b25591b3436ed996a4bb659b9dcf47576073d82f7275c95e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c7390210f8d25d19537f7aceb2903bed39e9368cd30b26149bc7aae1ea5d27`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:31 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 24 Feb 2026 19:25:31 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 24 Feb 2026 19:25:31 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 24 Feb 2026 19:25:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:25:31 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 24 Feb 2026 19:25:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:25:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:25:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:25:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:25:31 GMT
CMD []
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b087bfac04537947423e8ff107a4f236b18cb476414342ad978e5ef5d73d1d`  
		Last Modified: Tue, 24 Feb 2026 19:25:42 GMT  
		Size: 70.3 MB (70299489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17976d1518256f4737b5043d61fc260e90023c61b3c4d7bfc4b8333ff183f57`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c4ab11054961cf73452cfd2b2a9424613d6514b56077efab4dfcfdc2d2f820e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc0968bbdbc8ec3b5d5f035a557a0d639903e75b413f65653ed119c0af2a883`

```dockerfile
```

-	Layers:
	-	`sha256:799e51c9e22c3ee6ea2573b53b2e5a65d3891bd821601f3767c2499079ae01ae`  
		Last Modified: Tue, 24 Feb 2026 19:25:41 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.16`

```console
$ docker pull varnish@sha256:b61dde4047098837f0b22b0855e57ce01797471f586e377cd559197c50627412
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.16` - linux; amd64

```console
$ docker pull varnish@sha256:550aac2613064f8ae7e2355c72b60120ed40dfe110b65fa2ab70c4b0eb221579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4d432dcec47aa9b3913e33012f8bfde2d364e2c04a752509be48349185e06d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:07 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 24 Feb 2026 19:20:07 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 24 Feb 2026 19:20:07 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 24 Feb 2026 19:20:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:20:07 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 24 Feb 2026 19:20:07 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:20:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:20:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:20:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:20:07 GMT
CMD []
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5270969c016ab948ef843d0dafc3c5da8d1fb773ecdb3b6e1501b1861f1201a`  
		Last Modified: Tue, 24 Feb 2026 19:20:19 GMT  
		Size: 75.3 MB (75320899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed68ad79d2d4bcf843f875ee25a8f4997444cf992e8efb948fa9c61fca5b66`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:3b87f58b049ceae137f9e6c0ccd8288ba475fb634bc454689b939886c2938a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502c1825474e56e1445ffe978ab749d5025dcad4e05373a6322e35cb83980c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f9ec876009f49e3cb189387a17dc50137918fc09afc295f466f03ae4a3bac3ec`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 12.7 KB (12655 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1de539549e9d9b25591b3436ed996a4bb659b9dcf47576073d82f7275c95e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c7390210f8d25d19537f7aceb2903bed39e9368cd30b26149bc7aae1ea5d27`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:31 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 24 Feb 2026 19:25:31 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 24 Feb 2026 19:25:31 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 24 Feb 2026 19:25:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:25:31 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 24 Feb 2026 19:25:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:25:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:25:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:25:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:25:31 GMT
CMD []
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b087bfac04537947423e8ff107a4f236b18cb476414342ad978e5ef5d73d1d`  
		Last Modified: Tue, 24 Feb 2026 19:25:42 GMT  
		Size: 70.3 MB (70299489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17976d1518256f4737b5043d61fc260e90023c61b3c4d7bfc4b8333ff183f57`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:c4ab11054961cf73452cfd2b2a9424613d6514b56077efab4dfcfdc2d2f820e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc0968bbdbc8ec3b5d5f035a557a0d639903e75b413f65653ed119c0af2a883`

```dockerfile
```

-	Layers:
	-	`sha256:799e51c9e22c3ee6ea2573b53b2e5a65d3891bd821601f3767c2499079ae01ae`  
		Last Modified: Tue, 24 Feb 2026 19:25:41 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:fef29186771a0acf8f4fd154c5dd2e10fc7481f8968fee580162dd299aab51a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7` - linux; amd64

```console
$ docker pull varnish@sha256:1d91bf5bdfcd7ebf49c398380e2ae4aace319fd01b8f502297ae945e42b54d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfa63d6c3bf9dde5251daa524ba7239f384ed73a008ffe6d6b4c7a7e0bba491`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:34 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 24 Feb 2026 19:20:34 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 24 Feb 2026 19:20:34 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:20:34 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:20:35 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:20:35 GMT
USER varnish
# Tue, 24 Feb 2026 19:20:35 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:20:35 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2207dafc36b94660d9e9f904798f0f3085316a4bec5cda0b6b8c83516e529fa`  
		Last Modified: Tue, 24 Feb 2026 19:20:47 GMT  
		Size: 86.6 MB (86565611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c43e60dcbaa1d09500e307353504ae6e764b2cdfea10dfcac6db3e55a1e252`  
		Last Modified: Tue, 24 Feb 2026 19:20:45 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:779d84b3f9e33a42dd8a3ee184e1d57c572f26e17634e3dfb6ba0152053bbbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6dbc82a9233631ff82a8095286e832709fc2158b32f08f8132be3b25772d10`

```dockerfile
```

-	Layers:
	-	`sha256:e1029c251687c223c37f5b6a42db0fbe5897bb2b136b85baffd38f38a0959cd9`  
		Last Modified: Tue, 24 Feb 2026 19:20:45 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7ba80b185b0a62f98793cc84960da4f92bf61d8e8cd721a55fe382e782aca320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129d37c5507fc590c53799d45ea6d65da25b048d3e2bc1282317d38b6f44509`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:25:42 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 24 Feb 2026 19:25:42 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 24 Feb 2026 19:25:42 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:25:42 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:25:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:25:42 GMT
USER varnish
# Tue, 24 Feb 2026 19:25:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:25:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d2336431bd52587f8c32d2a2cc86239580ad7f5430e296f2ba42140dd0570`  
		Last Modified: Tue, 24 Feb 2026 19:25:54 GMT  
		Size: 80.4 MB (80384867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d99ce60e59c088218b55f8b4a5a507e4d2836d37a4b38a234675a7b6d8a6f9`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a26549872114770fefb7b4e6154c718a738a12066a48adc8af8580f0ede117`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:e14723e2167f3e6827a9fcb01eb2d44a2226f1f52816b45ad089f4e863de94d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275b1589e1e899036e8e0cb0a3ac4cf458b34dbc48412c5db94cb23a0e40b15b`

```dockerfile
```

-	Layers:
	-	`sha256:f698ec23329ee8aac3472df9cc6c9b0cb6ecd5b405ce38e472cafc527a4accc0`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
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
$ docker pull varnish@sha256:fef29186771a0acf8f4fd154c5dd2e10fc7481f8968fee580162dd299aab51a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:7.7.3` - linux; amd64

```console
$ docker pull varnish@sha256:1d91bf5bdfcd7ebf49c398380e2ae4aace319fd01b8f502297ae945e42b54d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfa63d6c3bf9dde5251daa524ba7239f384ed73a008ffe6d6b4c7a7e0bba491`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:34 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 24 Feb 2026 19:20:34 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 24 Feb 2026 19:20:34 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:20:34 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:20:35 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:20:35 GMT
USER varnish
# Tue, 24 Feb 2026 19:20:35 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:20:35 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2207dafc36b94660d9e9f904798f0f3085316a4bec5cda0b6b8c83516e529fa`  
		Last Modified: Tue, 24 Feb 2026 19:20:47 GMT  
		Size: 86.6 MB (86565611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c43e60dcbaa1d09500e307353504ae6e764b2cdfea10dfcac6db3e55a1e252`  
		Last Modified: Tue, 24 Feb 2026 19:20:45 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:779d84b3f9e33a42dd8a3ee184e1d57c572f26e17634e3dfb6ba0152053bbbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6dbc82a9233631ff82a8095286e832709fc2158b32f08f8132be3b25772d10`

```dockerfile
```

-	Layers:
	-	`sha256:e1029c251687c223c37f5b6a42db0fbe5897bb2b136b85baffd38f38a0959cd9`  
		Last Modified: Tue, 24 Feb 2026 19:20:45 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7ba80b185b0a62f98793cc84960da4f92bf61d8e8cd721a55fe382e782aca320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129d37c5507fc590c53799d45ea6d65da25b048d3e2bc1282317d38b6f44509`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:25:42 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 24 Feb 2026 19:25:42 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 24 Feb 2026 19:25:42 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:25:42 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:25:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:25:42 GMT
USER varnish
# Tue, 24 Feb 2026 19:25:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:25:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d2336431bd52587f8c32d2a2cc86239580ad7f5430e296f2ba42140dd0570`  
		Last Modified: Tue, 24 Feb 2026 19:25:54 GMT  
		Size: 80.4 MB (80384867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d99ce60e59c088218b55f8b4a5a507e4d2836d37a4b38a234675a7b6d8a6f9`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a26549872114770fefb7b4e6154c718a738a12066a48adc8af8580f0ede117`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:e14723e2167f3e6827a9fcb01eb2d44a2226f1f52816b45ad089f4e863de94d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275b1589e1e899036e8e0cb0a3ac4cf458b34dbc48412c5db94cb23a0e40b15b`

```dockerfile
```

-	Layers:
	-	`sha256:f698ec23329ee8aac3472df9cc6c9b0cb6ecd5b405ce38e472cafc527a4accc0`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
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
$ docker pull varnish@sha256:0e1132c6e36ff88eabf3dcc51210beb1c3f9d333a361802e027bf4333c8891a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:bcd81bb982780276a9e40822fc73e38697877c94c1ba7c8f683e277ddf6e2c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121964585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf7ee14cdb6aa767de5239e763f04537960d468ac3d8f40ae9a0ccebf5a949`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:19:31 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:19:31 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:19:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:19:31 GMT
USER varnish
# Tue, 24 Feb 2026 19:19:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:19:31 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c90ea41f762a289f21d4c77178a6923a6bde3566164188baf12f5c32318b60e`  
		Last Modified: Tue, 24 Feb 2026 19:19:45 GMT  
		Size: 92.2 MB (92182834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ceb97c3457eaadb115eaeb93e50bcc9398bca7b015db68e943c545e7e10337`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe373b29e6214b8e3b0f2bf583630b0a072fe28d26feef152f0a95b2adc2f2f1`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:f3cdcbd1a604471fe349b51e7a7ec413613688ef59a48bdfd81f6ff974b09744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569f775851aa56a6c9957051ea1a3fb40f1ad60feadc65df5e4d8ec78a17925`

```dockerfile
```

-	Layers:
	-	`sha256:cdf500b595e2e1ec85d49c5d62c6a1bdd3f9b42a990de8223f0068c6b69faf90`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 20.9 KB (20876 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:99e7eec48c7cf7b92aef7e6b337069855e47367a388858cd15c34f49f1e3e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115939806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c48f27a9c62f7325a81fc6fc3e035515bb856d63e7ee2c09c84c1f7392faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:24:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:24:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:24:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:24:33 GMT
USER varnish
# Tue, 24 Feb 2026 19:24:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:24:33 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56094c358efb778511d7bbc7a37bc154e95f75de478b38d6335404adfbaf4e5b`  
		Last Modified: Tue, 24 Feb 2026 19:24:46 GMT  
		Size: 85.8 MB (85796589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80ff03b3a4b59b0d277baaa1c5c43c0fad125035e10852ee96385e0b579ed6`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cfbdc19e0b2635c7ed87d16bb781c8d6912853949b27d1604213bb1e4e963`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61562a1276f3b2423989c742dc37c1ad3a656cec3dd59fdcb0dd0846bd59c8`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:33143720bbbef1a9041a0d48f1ccd42825f68039318b827c574087461defa3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de93c55ebce55f06702f402c18a7d9add3ccd2bb8518b4b8dd7ef59a455682d`

```dockerfile
```

-	Layers:
	-	`sha256:b37c0664e8aea846dd1776198b8fe5954acdee0dbffe08176f134e75f67bf48c`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
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
$ docker pull varnish@sha256:0e1132c6e36ff88eabf3dcc51210beb1c3f9d333a361802e027bf4333c8891a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:bcd81bb982780276a9e40822fc73e38697877c94c1ba7c8f683e277ddf6e2c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121964585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf7ee14cdb6aa767de5239e763f04537960d468ac3d8f40ae9a0ccebf5a949`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:19:31 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:19:31 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:19:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:19:31 GMT
USER varnish
# Tue, 24 Feb 2026 19:19:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:19:31 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c90ea41f762a289f21d4c77178a6923a6bde3566164188baf12f5c32318b60e`  
		Last Modified: Tue, 24 Feb 2026 19:19:45 GMT  
		Size: 92.2 MB (92182834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ceb97c3457eaadb115eaeb93e50bcc9398bca7b015db68e943c545e7e10337`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe373b29e6214b8e3b0f2bf583630b0a072fe28d26feef152f0a95b2adc2f2f1`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f3cdcbd1a604471fe349b51e7a7ec413613688ef59a48bdfd81f6ff974b09744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569f775851aa56a6c9957051ea1a3fb40f1ad60feadc65df5e4d8ec78a17925`

```dockerfile
```

-	Layers:
	-	`sha256:cdf500b595e2e1ec85d49c5d62c6a1bdd3f9b42a990de8223f0068c6b69faf90`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 20.9 KB (20876 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:99e7eec48c7cf7b92aef7e6b337069855e47367a388858cd15c34f49f1e3e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115939806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c48f27a9c62f7325a81fc6fc3e035515bb856d63e7ee2c09c84c1f7392faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:24:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:24:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:24:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:24:33 GMT
USER varnish
# Tue, 24 Feb 2026 19:24:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:24:33 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56094c358efb778511d7bbc7a37bc154e95f75de478b38d6335404adfbaf4e5b`  
		Last Modified: Tue, 24 Feb 2026 19:24:46 GMT  
		Size: 85.8 MB (85796589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80ff03b3a4b59b0d277baaa1c5c43c0fad125035e10852ee96385e0b579ed6`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cfbdc19e0b2635c7ed87d16bb781c8d6912853949b27d1604213bb1e4e963`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61562a1276f3b2423989c742dc37c1ad3a656cec3dd59fdcb0dd0846bd59c8`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:33143720bbbef1a9041a0d48f1ccd42825f68039318b827c574087461defa3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de93c55ebce55f06702f402c18a7d9add3ccd2bb8518b4b8dd7ef59a455682d`

```dockerfile
```

-	Layers:
	-	`sha256:b37c0664e8aea846dd1776198b8fe5954acdee0dbffe08176f134e75f67bf48c`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
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
$ docker pull varnish@sha256:0e1132c6e36ff88eabf3dcc51210beb1c3f9d333a361802e027bf4333c8891a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.0` - linux; amd64

```console
$ docker pull varnish@sha256:bcd81bb982780276a9e40822fc73e38697877c94c1ba7c8f683e277ddf6e2c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121964585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf7ee14cdb6aa767de5239e763f04537960d468ac3d8f40ae9a0ccebf5a949`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:19:31 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:19:31 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:19:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:19:31 GMT
USER varnish
# Tue, 24 Feb 2026 19:19:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:19:31 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c90ea41f762a289f21d4c77178a6923a6bde3566164188baf12f5c32318b60e`  
		Last Modified: Tue, 24 Feb 2026 19:19:45 GMT  
		Size: 92.2 MB (92182834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ceb97c3457eaadb115eaeb93e50bcc9398bca7b015db68e943c545e7e10337`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe373b29e6214b8e3b0f2bf583630b0a072fe28d26feef152f0a95b2adc2f2f1`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:f3cdcbd1a604471fe349b51e7a7ec413613688ef59a48bdfd81f6ff974b09744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569f775851aa56a6c9957051ea1a3fb40f1ad60feadc65df5e4d8ec78a17925`

```dockerfile
```

-	Layers:
	-	`sha256:cdf500b595e2e1ec85d49c5d62c6a1bdd3f9b42a990de8223f0068c6b69faf90`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 20.9 KB (20876 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:99e7eec48c7cf7b92aef7e6b337069855e47367a388858cd15c34f49f1e3e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115939806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c48f27a9c62f7325a81fc6fc3e035515bb856d63e7ee2c09c84c1f7392faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:24:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:24:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:24:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:24:33 GMT
USER varnish
# Tue, 24 Feb 2026 19:24:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:24:33 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56094c358efb778511d7bbc7a37bc154e95f75de478b38d6335404adfbaf4e5b`  
		Last Modified: Tue, 24 Feb 2026 19:24:46 GMT  
		Size: 85.8 MB (85796589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80ff03b3a4b59b0d277baaa1c5c43c0fad125035e10852ee96385e0b579ed6`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cfbdc19e0b2635c7ed87d16bb781c8d6912853949b27d1604213bb1e4e963`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61562a1276f3b2423989c742dc37c1ad3a656cec3dd59fdcb0dd0846bd59c8`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:33143720bbbef1a9041a0d48f1ccd42825f68039318b827c574087461defa3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de93c55ebce55f06702f402c18a7d9add3ccd2bb8518b4b8dd7ef59a455682d`

```dockerfile
```

-	Layers:
	-	`sha256:b37c0664e8aea846dd1776198b8fe5954acdee0dbffe08176f134e75f67bf48c`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
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
$ docker pull varnish@sha256:0e1132c6e36ff88eabf3dcc51210beb1c3f9d333a361802e027bf4333c8891a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:bcd81bb982780276a9e40822fc73e38697877c94c1ba7c8f683e277ddf6e2c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121964585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf7ee14cdb6aa767de5239e763f04537960d468ac3d8f40ae9a0ccebf5a949`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:19:31 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:19:31 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:19:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:19:31 GMT
USER varnish
# Tue, 24 Feb 2026 19:19:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:19:31 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c90ea41f762a289f21d4c77178a6923a6bde3566164188baf12f5c32318b60e`  
		Last Modified: Tue, 24 Feb 2026 19:19:45 GMT  
		Size: 92.2 MB (92182834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ceb97c3457eaadb115eaeb93e50bcc9398bca7b015db68e943c545e7e10337`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe373b29e6214b8e3b0f2bf583630b0a072fe28d26feef152f0a95b2adc2f2f1`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:f3cdcbd1a604471fe349b51e7a7ec413613688ef59a48bdfd81f6ff974b09744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569f775851aa56a6c9957051ea1a3fb40f1ad60feadc65df5e4d8ec78a17925`

```dockerfile
```

-	Layers:
	-	`sha256:cdf500b595e2e1ec85d49c5d62c6a1bdd3f9b42a990de8223f0068c6b69faf90`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 20.9 KB (20876 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:99e7eec48c7cf7b92aef7e6b337069855e47367a388858cd15c34f49f1e3e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115939806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c48f27a9c62f7325a81fc6fc3e035515bb856d63e7ee2c09c84c1f7392faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:24:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:24:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:24:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:24:33 GMT
USER varnish
# Tue, 24 Feb 2026 19:24:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:24:33 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56094c358efb778511d7bbc7a37bc154e95f75de478b38d6335404adfbaf4e5b`  
		Last Modified: Tue, 24 Feb 2026 19:24:46 GMT  
		Size: 85.8 MB (85796589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80ff03b3a4b59b0d277baaa1c5c43c0fad125035e10852ee96385e0b579ed6`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cfbdc19e0b2635c7ed87d16bb781c8d6912853949b27d1604213bb1e4e963`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61562a1276f3b2423989c742dc37c1ad3a656cec3dd59fdcb0dd0846bd59c8`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:33143720bbbef1a9041a0d48f1ccd42825f68039318b827c574087461defa3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de93c55ebce55f06702f402c18a7d9add3ccd2bb8518b4b8dd7ef59a455682d`

```dockerfile
```

-	Layers:
	-	`sha256:b37c0664e8aea846dd1776198b8fe5954acdee0dbffe08176f134e75f67bf48c`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
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
$ docker pull varnish@sha256:0e1132c6e36ff88eabf3dcc51210beb1c3f9d333a361802e027bf4333c8891a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:bcd81bb982780276a9e40822fc73e38697877c94c1ba7c8f683e277ddf6e2c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121964585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf7ee14cdb6aa767de5239e763f04537960d468ac3d8f40ae9a0ccebf5a949`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:19:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:19:31 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:19:31 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:19:31 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:19:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:19:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:19:31 GMT
USER varnish
# Tue, 24 Feb 2026 19:19:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:19:31 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c90ea41f762a289f21d4c77178a6923a6bde3566164188baf12f5c32318b60e`  
		Last Modified: Tue, 24 Feb 2026 19:19:45 GMT  
		Size: 92.2 MB (92182834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ceb97c3457eaadb115eaeb93e50bcc9398bca7b015db68e943c545e7e10337`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe373b29e6214b8e3b0f2bf583630b0a072fe28d26feef152f0a95b2adc2f2f1`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:f3cdcbd1a604471fe349b51e7a7ec413613688ef59a48bdfd81f6ff974b09744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569f775851aa56a6c9957051ea1a3fb40f1ad60feadc65df5e4d8ec78a17925`

```dockerfile
```

-	Layers:
	-	`sha256:cdf500b595e2e1ec85d49c5d62c6a1bdd3f9b42a990de8223f0068c6b69faf90`  
		Last Modified: Tue, 24 Feb 2026 19:19:42 GMT  
		Size: 20.9 KB (20876 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:99e7eec48c7cf7b92aef7e6b337069855e47367a388858cd15c34f49f1e3e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115939806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c48f27a9c62f7325a81fc6fc3e035515bb856d63e7ee2c09c84c1f7392faf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-5
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 24 Feb 2026 19:24:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 24 Feb 2026 19:24:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:24:33 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:24:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.0-5 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:24:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:24:33 GMT
USER varnish
# Tue, 24 Feb 2026 19:24:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:24:33 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56094c358efb778511d7bbc7a37bc154e95f75de478b38d6335404adfbaf4e5b`  
		Last Modified: Tue, 24 Feb 2026 19:24:46 GMT  
		Size: 85.8 MB (85796589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80ff03b3a4b59b0d277baaa1c5c43c0fad125035e10852ee96385e0b579ed6`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cfbdc19e0b2635c7ed87d16bb781c8d6912853949b27d1604213bb1e4e963`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61562a1276f3b2423989c742dc37c1ad3a656cec3dd59fdcb0dd0846bd59c8`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:33143720bbbef1a9041a0d48f1ccd42825f68039318b827c574087461defa3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de93c55ebce55f06702f402c18a7d9add3ccd2bb8518b4b8dd7ef59a455682d`

```dockerfile
```

-	Layers:
	-	`sha256:b37c0664e8aea846dd1776198b8fe5954acdee0dbffe08176f134e75f67bf48c`  
		Last Modified: Tue, 24 Feb 2026 19:24:45 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:fef29186771a0acf8f4fd154c5dd2e10fc7481f8968fee580162dd299aab51a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:1d91bf5bdfcd7ebf49c398380e2ae4aace319fd01b8f502297ae945e42b54d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfa63d6c3bf9dde5251daa524ba7239f384ed73a008ffe6d6b4c7a7e0bba491`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:34 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 24 Feb 2026 19:20:34 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 24 Feb 2026 19:20:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 24 Feb 2026 19:20:34 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:20:34 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:20:34 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:20:35 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:20:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:20:35 GMT
USER varnish
# Tue, 24 Feb 2026 19:20:35 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:20:35 GMT
CMD []
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2207dafc36b94660d9e9f904798f0f3085316a4bec5cda0b6b8c83516e529fa`  
		Last Modified: Tue, 24 Feb 2026 19:20:47 GMT  
		Size: 86.6 MB (86565611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12a0569e59cafb68e401d4c73c76cbd5602ccb266cdae168ff4622d8c57e29`  
		Last Modified: Tue, 24 Feb 2026 19:19:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c43e60dcbaa1d09500e307353504ae6e764b2cdfea10dfcac6db3e55a1e252`  
		Last Modified: Tue, 24 Feb 2026 19:20:45 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:779d84b3f9e33a42dd8a3ee184e1d57c572f26e17634e3dfb6ba0152053bbbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6dbc82a9233631ff82a8095286e832709fc2158b32f08f8132be3b25772d10`

```dockerfile
```

-	Layers:
	-	`sha256:e1029c251687c223c37f5b6a42db0fbe5897bb2b136b85baffd38f38a0959cd9`  
		Last Modified: Tue, 24 Feb 2026 19:20:45 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7ba80b185b0a62f98793cc84960da4f92bf61d8e8cd721a55fe382e782aca320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129d37c5507fc590c53799d45ea6d65da25b048d3e2bc1282317d38b6f44509`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:25:42 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 24 Feb 2026 19:25:42 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 24 Feb 2026 19:25:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 24 Feb 2026 19:25:42 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:25:42 GMT
ENV VSM_NOPID=1
# Tue, 24 Feb 2026 19:25:42 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -L -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:25:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:25:42 GMT
USER varnish
# Tue, 24 Feb 2026 19:25:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:25:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d2336431bd52587f8c32d2a2cc86239580ad7f5430e296f2ba42140dd0570`  
		Last Modified: Tue, 24 Feb 2026 19:25:54 GMT  
		Size: 80.4 MB (80384867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d99ce60e59c088218b55f8b4a5a507e4d2836d37a4b38a234675a7b6d8a6f9`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a26549872114770fefb7b4e6154c718a738a12066a48adc8af8580f0ede117`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e14723e2167f3e6827a9fcb01eb2d44a2226f1f52816b45ad089f4e863de94d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275b1589e1e899036e8e0cb0a3ac4cf458b34dbc48412c5db94cb23a0e40b15b`

```dockerfile
```

-	Layers:
	-	`sha256:f698ec23329ee8aac3472df9cc6c9b0cb6ecd5b405ce38e472cafc527a4accc0`  
		Last Modified: Tue, 24 Feb 2026 19:25:52 GMT  
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
$ docker pull varnish@sha256:b61dde4047098837f0b22b0855e57ce01797471f586e377cd559197c50627412
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:550aac2613064f8ae7e2355c72b60120ed40dfe110b65fa2ab70c4b0eb221579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4d432dcec47aa9b3913e33012f8bfde2d364e2c04a752509be48349185e06d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:07 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 24 Feb 2026 19:20:07 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 24 Feb 2026 19:20:07 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 24 Feb 2026 19:20:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:20:07 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 24 Feb 2026 19:20:07 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:20:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:20:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:20:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:20:07 GMT
CMD []
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5270969c016ab948ef843d0dafc3c5da8d1fb773ecdb3b6e1501b1861f1201a`  
		Last Modified: Tue, 24 Feb 2026 19:20:19 GMT  
		Size: 75.3 MB (75320899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed68ad79d2d4bcf843f875ee25a8f4997444cf992e8efb948fa9c61fca5b66`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:3b87f58b049ceae137f9e6c0ccd8288ba475fb634bc454689b939886c2938a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502c1825474e56e1445ffe978ab749d5025dcad4e05373a6322e35cb83980c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f9ec876009f49e3cb189387a17dc50137918fc09afc295f466f03ae4a3bac3ec`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 12.7 KB (12655 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1de539549e9d9b25591b3436ed996a4bb659b9dcf47576073d82f7275c95e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c7390210f8d25d19537f7aceb2903bed39e9368cd30b26149bc7aae1ea5d27`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:31 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 24 Feb 2026 19:25:31 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 24 Feb 2026 19:25:31 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 24 Feb 2026 19:25:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 24 Feb 2026 19:25:31 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 24 Feb 2026 19:25:31 GMT
WORKDIR /etc/varnish
# Tue, 24 Feb 2026 19:25:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:25:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 24 Feb 2026 19:25:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 24 Feb 2026 19:25:31 GMT
CMD []
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b087bfac04537947423e8ff107a4f236b18cb476414342ad978e5ef5d73d1d`  
		Last Modified: Tue, 24 Feb 2026 19:25:42 GMT  
		Size: 70.3 MB (70299489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17976d1518256f4737b5043d61fc260e90023c61b3c4d7bfc4b8333ff183f57`  
		Last Modified: Tue, 24 Feb 2026 19:25:40 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:c4ab11054961cf73452cfd2b2a9424613d6514b56077efab4dfcfdc2d2f820e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc0968bbdbc8ec3b5d5f035a557a0d639903e75b413f65653ed119c0af2a883`

```dockerfile
```

-	Layers:
	-	`sha256:799e51c9e22c3ee6ea2573b53b2e5a65d3891bd821601f3767c2499079ae01ae`  
		Last Modified: Tue, 24 Feb 2026 19:25:41 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json
